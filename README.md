# Triart – Dashboard de Indicadores

Google Sheets → (Apps Script, de hora em hora) → Supabase → Dashboard HTML.

## Passo a passo
1. **Supabase**: crie o projeto e rode [supabase/schema.sql](supabase/schema.sql) no SQL Editor.
2. **Planilha**: crie as abas `Comercial`, `Projetos`, `Producao`, `RH`. Linha 1 = cabeçalhos, uma linha por mês.

   | Aba | Cabeçalhos |
   |---|---|
   | Comercial | Periodo, Leads Recebidos, Leads Convertidos, Propostas Enviadas, Tempo Medio de Fechamento |
   | Projetos | Periodo, Solicitados, Finalizados, Alterados |
   | Producao | Periodo, Acuracidade Almoxarifado / Vidro / Sodem / Perfil / Eletrico, Perdas e Extravios |
   | RH | Periodo, Turnover, Absenteismo, Feedbacks, PCO |

   `Periodo` aceita `09/2026`, `01/09/2026` ou `2026-09`. Percentuais podem vir como `95,5%` ou `95,5`.
3. **Sincronização**: cole [google-sheets/Sync.gs](google-sheets/Sync.gs) em Extensões > Apps Script, defina as propriedades `SUPABASE_URL` e `SUPABASE_SERVICE_KEY`, rode `syncAll()` para testar e `setupTrigger()` para automatizar.
4. **Dashboard**: em [dashboard/index.html](dashboard/index.html) preencha `SUPABASE_URL` e `SUPABASE_ANON_KEY` (topo do script) e publique (Netlify, Vercel, GitHub Pages…). Sem as chaves, abre em modo demonstração com dados fictícios.

## Regras de exibição
- Referência = mês atual. Se o mês ainda não tem dados, o card mostra o último mês disponível e indica "ref. mês/ano".
- Gráficos mostram os últimos 12 meses; linha tracejada = meta.
- Finalização de projetos (cartão e pizza) soma todos os períodos; perdas e extravios = média do ano corrente.
- Taxa de conversão = Leads Convertidos ÷ Leads Recebidos; % finalizados = Finalizados ÷ Solicitados.

## Segurança
A chave `service_role` fica **somente** no Apps Script. O HTML usa a `anon`, limitada a leitura por RLS – quem tiver o link do dashboard consegue ler os dados. Para restringir, adicione Supabase Auth ou hospede atrás de login.
