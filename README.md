# Insight Hub

Imagine que você seja um consultor em um projeto. Você deve criar um Dashboard em HTML que seja automatizado, ou seja, toda vez que houver um input na planilha do google sheets (Base de dados) o dashboard é atualizado. Existem 4 áreas com seus respectivos indicadores para serem demonstrados no dashboard.

Área Comercial:




Base de dados (Colunas):ID; Data de Entrada do Lead; Cliente / Empresa; Origem do Lead; Vendedor Responsável; Valor Estimado (R$); Status do Lead; Data de Conversão/Perda; Motivo (se Perdido); Data de Envio da Proposta; Valor da Proposta (R$); Status da Proposta; Data de Retorno do Cliente; Data de Fechamento (Venda Ganha); Valor da Venda (R$).

Indicadores:

Taxa de conversão de Leads (meta 70%): Gráfico de linha temporal mostrando a evolução da taxa de conversão no tempo.

Volume de propostas Enviadas: Gráfico em barras mostrando o volume de propostas enviadas por período. Gráfico de pizza da participação do mês no valor total de propostas.

Tempo médio de fechamento: Gráfico de linha temporal do tempo médio de fechamento por período.




Área Projetos: 




Base de dados (Colunas): Mês; Projetos Solicitados (nº); Projetos Finalizados (nº); % Finalizados vs Solicitados; Alterações (nº); % Alterações vs Solicitados

Indicadores:

Finalização de projetos: Cartão com total de projetos solicitados e projetos finalizados em todos os períodos; Gráfico de pizza mostrando a porcentagem de projetos finalizados dos projetos solicitados. Gráfico de linha mostrando a evolução temporal da % Finalizados vs Solicitados ao longo dos meses.

Alterações de projetos: Gráfico de colunas mostrando o número de projetos alterados por período. 




Área Produção:




Base de dados (Colunas):

Aba de Almoxarifado: Período; Estoque Contado (un.); Estoque no Sistema (un.); Meta (%)

Aba de Vidros: Período; Estoque Contado (un.); Estoque no Sistema (un.); Meta (%)

Aba de Sodem: Período; Estoque Contado (un.); Estoque no Sistema (un.); Meta (%)

Aba de Perfil: Período; Estoque Contado (un.); Estoque no Sistema (un.); Meta (%)

Aba de Elétrico: Período; Estoque Contado (un.); Estoque no Sistema (un.); Meta (%)

Aba de Perdas e Extrativos: Evento; Valor de Perdas/Extravios (R$); Valor Total do Estoque (R$); Meta (%)

Indicadores:

Acuracidade Almoxarifado (Meta 95%): Gráfico de linha mostrando a evolução da acuracidade do estoque por período.

Acuracidade Vidro (Meta 95%): Gráfico de linha mostrando a evolução da acuracidade do estoque por período.

Acuracidade Sodem (Meta 95%): Gráfico de linha mostrando a evolução da acuracidade do estoque por período.

Acuracidade Perfil (Meta 95%): Gráfico de linha mostrando a evolução da acuracidade do estoque por período.

Acuracidade Elétrico (Meta 95%): Gráfico de linha mostrando a evolução da acuracidade do estoque por período.

Perdas e Extrativos (Meta 5%): Gráfico de colunas mostrando a porcentagem do Valor de Perdas/Extravios (R$) vs Valor Total do Estoque (R$) por evento.




Área RH




Base de Dados (Colunas): Indicador; Polaridade; Meta; Jan; Fev; Mar; Abr; Mai; Jun; Jul; Ago; Set; Out; Nov; Dez; Média Anual.

Indicadores:

Taxa de turnover (meta 5%): Gráfico de linha mostrando a evolução temporal da taxa de turnover

Taxa de absenteísmo (meta 3%):Gráfico de linha mostrando a evolução temporal da taxa de absenteísmo.

This project was built with [Lovable](https://lovable.dev).

**Live app**: https://auto-sheet-viz.lovable.app

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/fa4d6783-d565-4612-874a-c59fede4d32c).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
