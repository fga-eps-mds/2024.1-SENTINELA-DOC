# Integração e deploy contínuos

## Deploy contínuo

Foram utilizadas três diferentes plataformas para hospedar a arquitetura do sistema. Primeiramente, foi escolhido o **Netlify** para a hospedagem do Frontend. A plataforma é simples e intuitiva, além de permitir a conexão com deploy contínuo de branches específicas, permitindo a criação de um ambiente de homologação das histórias.

Considerando a arquitetura do sistema organizada em microsserviços foi necessário que o deploy de backends seguisse o mesmo formato. Além disso, a plataforma **Render** não permitia a hospedagem dos bancos de dados de forma gratuita. Assim, foram criadas três instâncias separadas no render, contendo cada um dos backends utilizados: Usuários, Financeiro e Benefícios.

Por fim, os bancos de dados foram hospedados no **Mongo Atlas**, permitindo maior facilidade de acesso ao banco para verificar possíveis inconsistências sem necessidade de custos adicionais.

A conexão entre frontend e backend foi feita pela utilização de variáveis de ambiente facilmente configuráveis para endereçar os endpoints necessários. De forma similar, foi feita a conexão de cada um dos backends com seu respectivo banco de dados.

## Integração contínua

Para a integração contínua do projeto, foi criado um pipeline de CI que executava jobs de checagem de lint, format, build, test e sonarcloud. Isto é, o workflow confere se o código está dentro dos padrões de formatação definidos, se está sendo _buildado_ corretamente, se todos os testes estão passado e se as métricas foram enviadas para o Sonar.

Além disso, foi criado um pipeline de Release, para ser rodado sempre que fosse realizado um push na main e pull requests fechados na devel e main, o qual gera arquivo JSON de métricas do repositório toda vez que uma Release é entregue. Esses arquivos de métricas foram usados posteriormente no Notebook Analytics, para criar uma visualização do andamento do projeto.

### Frontend

| Métrica                                                     | Medida |
| ----------------------------------------------------------- | ------ |
| Quantidade de vezes que o pipeline de CI foi executado      | 439    |
| Quantidade de vezes que o pipeline de CI falhou             | 125    |
| Quantidade de vezes que o pipeline de Release foi executado | 62     |
| Quantidade de vezes que o pipeline de Release falhou        | 26     |
| Quantidade de PRs abertos                                   | 69     |
| Quantidade de PRs revisados                                 | 36     |
| Quantidade de Releases                                      | 5      |

### Backend Usuários

| Métrica                                                     | Medida |
| ----------------------------------------------------------- | ------ |
| Quantidade de vezes que o pipeline de CI foi executado      | 103    |
| Quantidade de vezes que o pipeline de CI falhou             | 24     |
| Quantidade de vezes que o pipeline de Release foi executado | 34     |
| Quantidade de vezes que o pipeline de Release falhou        | 14     |
| Quantidade de PRs abertos                                   | 37     |
| Quantidade de PRs revisados                                 | 15     |
| Quantidade de Releases                                      | 5      |

### Backend Benefícios

| Métrica                                                     | Medida |
| ----------------------------------------------------------- | ------ |
| Quantidade de vezes que o pipeline de CI foi executado      | 35     |
| Quantidade de vezes que o pipeline de CI falhou             | 9      |
| Quantidade de vezes que o pipeline de Release foi executado | 12     |
| Quantidade de vezes que o pipeline de Release falhou        | 2      |
| Quantidade de PRs abertos                                   | 7      |
| Quantidade de PRs revisados                                 | 7      |
| Quantidade de Releases                                      | 1      |

### Backend Financeiro

| Métrica                                                     | Medida |
| ----------------------------------------------------------- | ------ |
| Quantidade de vezes que o pipeline de CI foi executado      | 106    |
| Quantidade de vezes que o pipeline de CI falhou             | 19     |
| Quantidade de vezes que o pipeline de Release foi executado | 23     |
| Quantidade de vezes que o pipeline de Release falhou        | 2      |
| Quantidade de PRs abertos                                   | 20     |
| Quantidade de PRs revisados                                 | 10     |
| Quantidade de Releases                                      | 3      |

Com relação às falhas do pipeline de CI, estas se devem em maior parte aos _flaky tests_, que foram um problema enfrentado pelo time durante algumas semanas. Os testes passavam localmente e na maior parte das vezes também passava no pipeline, entretanto falhava em alguns momentos. Esse problema, no entanto, foi corrigido nas últimas semanas e não voltou a ser notado pelos membros. Ressalta-se que alguns pipelines também falharam por testes que estavam quebrados e problemas de formatação, que sempre foram encaminhados para resolução até que não falhassem mais.

Quanto aos pipelines de Release, as falhas inicialmente são referentes a configuração equivocada do arquivo sonar-metrics.py, que não estava configurado corretamente para receber branches e tags (versões). Esse pipeline também sofreu alterações quanto à definição de quando deveria ser executado, conforme apontamento do professor.

## Histórico de Versões

| Alteração            | Data     | Autor                                        |
| -------------------- | -------- | -------------------------------------------- |
| Criação do documento | 08/09/24 | Ingrid Carvalho, Alvaro Gouvea e Sara Campos |
