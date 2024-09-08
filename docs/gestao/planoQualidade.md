# Plano de Qualidade


## Introdução

De acordo com a ISO 25010, a qualidade de um produto de software é definida pelo grau em que ele atende aos requisitos de seus usuários, agregando valor. Esses requisitos, que incluem funcionalidade, desempenho, segurança, manutenibilidade, entre outros, são representados no modelo de qualidade, que categoriza a qualidade do produto em características e subcaracterísticas. Para alcançar esses requisitos, é essencial desenvolver e monitorar métricas de forma contínua. O objetivo do planejamento de qualidade é descrever como esse monitoramento foi realizado durante o projeto.

## Processo de Qualidade

Para garantir a qualidade do projeto, integramos cada serviço desenvolvido com a ferramenta SonarQube, utilizando a interface SonarCloud para proporcionar uma análise mais amigável e detalhada de todas as métricas coletadas. O processo é orientado pela validação das US com o cliente, utilizando protótipos e critérios de aceitação, seguido pela implementação contínua de melhorias. Após o desenvolvimento, as funcionalidades passam pelos testes de aceitação conduzidos pelo cliente, assegurando que ajustes e aperfeiçoamentos sejam aplicados. Caso novas melhorias sejam identificadas, elas são incorporadas ao processo de desenvolvimento, reforçando a qualidade do produto.

<p align="center">
  <img src="https://github.com/user-attachments/assets/bd21595f-81ea-46ab-ba02-123a3e4f390f" alt="eps qualidade">
</p>

## Métricas Monitoradas:
* Cobertura de Código
* Duplicação de Código
* Vulnerabilidades e Bugs
* Integração com CI/CD: Configuração do SonarCloud com pipelines de integração contínua.
* Alertas e Relatórios: Configuração de thresholds para alertas automáticos e geração de relatórios.

## Políticas de Código e Revisão
* Pull Requests e Code Review: Processo de revisão de código e melhores práticas para garantir qualidade.
* Padrões de Codificação: Ferramentas e regras aplicadas para padronização do código.
* Merge Guidelines: Critérios para fusão de branches e deploy.

## Ferramentas de Teste 
**Vitest**: Framework de testes rápido e leve, projetado para o ecossistema JavaScript, com foco em integração com Vite. Suporta mocks, TypeScript e testes ESM, acelerando o desenvolvimento front-end.

**SonarCloud**: plataforma de análise de código que identifica bugs, vulnerabilidades e code smells. Oferece suporte a várias linguagens, integrando-se facilmente ao fluxo CI/CD para garantir a qualidade do código.

**ZenHub**: ferramenta de gerenciamento de projetos que se integra ao GitHub, oferecendo recursos como quadros kanban e relatórios de produtividade

## Acompanhamento de métricas do sonar

### Release 1
Funcionalidades presentes:
- US01 - Fazer login
- US02 - Solicitar filiação
- US04 - Cadastrar usuários
- US33 - Atualizar dados de usuário
  
### Release 2
Funcionalidades presentes:
- US02 - Solicitar filiação (Ajustes pedidos na Release 1)
- US19- Cadastrar benefícios
- US34 - Gerenciar filiações
  
### Release 3
Funcionalidades presentes:
- US03 - Cadastrar fornecedores
- US05 - Cadastrar contas bancárias
- US17 - Cadastrar perfis no sistema

### Release MVP
Funcionalidades presentes:
- US01 - Fazer login no sistema (Ajustes pedidos na Release 1)
- US03 - Cadastrar fornecedores (Ajustes pedidos na Release 3)
- US16 - Visualizar dashboard sobre os sindicalizados
- US20 - Cadastrar movimentações financeiras
- US23 - Consulta do Histórico de Contribuições do sindicalizado
- US35 - Cadastro de órgão/lotação
- US34 - Gerenciar solicitações de filiação (Ajustes pedidos na Release 2)


# Modelo de Qualidade do Q-Rapids
Foi escolhido a plataforma de apoio à decisão voltada para o desenvolvimento ágil de software,  Q-Rapids. Ele foi projetado para auxiliar equipes de desenvolvimento a tomar decisões informadas com base em métricas de qualidade e dados em tempo real, coletados automaticamente ao longo do ciclo de vida do software. O Q-Rapids integra diferentes fontes de informação, como ferramentas de gestão de projetos, controle de versão e sistemas de integração contínua, para gerar relatórios e dashboards que oferecem uma visão detalhada sobre a saúde do projeto. Seu objetivo principal é melhorar a qualidade do software, facilitar a gestão de riscos e otimizar processos, permitindo que as equipes sejam mais ágeis e eficazes na entrega de software.

Os fatores e métricas de qualidade são critérios usados para avaliar a eficiência, desempenho e confiabilidade de um produto de software, seu processo de desenvolvimento e a organização como um todo. Esses fatores, como manutenibilidade, confiabilidade, usabilidade e eficiência, ajudam a medir quão bem o software atende aos requisitos técnicos e às expectativas dos usuários. As métricas associadas fornecem dados quantitativos que permitem monitorar e melhorar a qualidade continuamente. Utilizá-las é essencial para identificar problemas precocemente, aumentar a satisfação do cliente, reduzir custos com retrabalho e garantir o alinhamento do produto com os objetivos estratégicos da organização.

### Métricas

As métricas definidas para o Sentinela foram:

| Métrica                  | Descrição                                           |
| ------------------------ | --------------------------------------------------- |
| Files                    | Quantidade de arquivos de código                    |
| Functions                | Quantidade de funções no código                     |
| Complexity               | Complexidade ciclomática                            |
| Comment Lines Density    | Densidade (%) de linhas comentadas                  |
| Duplicated Lines density | Densidade (%) de linhas duplicadas                  |
| Coverage                 | Cobertura de código pelos testes                    |
| Ncloc                    | Quantidade de linhas de código                      |
| Tests                    | Testes unitários e de integração                    |
| Test Errors              | Testes que possuem erros                            |
| Test Failures            | Testes que falharam                                 |
| Test Execution Time      | Tempo de execução dos testes                        |
| Security Rating          | Avaliação de segurança de falhas e vulnerabilidades |

### Métricas para o produto

O uso de métricas permite identificar subcaracterísticas associadas e avaliar a qualidade do produto. Essa análise também possibilita medir a produtividade do projeto, gerando resultados que influenciam as decisões de desenvolvimento. Com base nas métricas especificadas no SonarCloud e Q-Rapids, além dos dados coletados, foram definidos os valores mínimos aceitáveis para cada métrica no projeto Sentinela, conforme mostrado nas tabelas abaixo.

#### Repositório do Frontend
| Métrica                      | Valor referência | Valor alcançado|
| ---------------------------- | ------------     |----------------|
| Complexity                   | até 10           |       1,408    |
| Comment Lines Density (%)    | até 30%          |       1,9%     |
| Duplicated Lines Density (%) | até 5%           |       7%       |
| Coverage                     | acima de 80%     |       78,1%    |
| Test Failures                | 0                |       0        |
| Test Errors                  | 0                |       0        |
| Security Rating              | 0 (A)            |       0(A)     |
| Satisfação do usuário        | acima de 3       ||

#### Repositório do Backend - Usuários
| Métrica                      | Valor referência | Valor alcançado|
| ---------------------------- | ------------     |-----------------|
| Complexity                   | até 10           |     112         |
| Comment Lines Density (%)    | até 30%          |     4,7%        |
| Duplicated Lines Density (%) | até 5%           |     0,0%        |
| Coverage                     | acima de 80%     |     78,2        |
| Test Failures                | 0                |     0           |
| Test Errors                  | 0                |     0           |
| Security Rating              | 0 (A)            |     0(A)        |
| Satisfação do usuário        | acima de 3       |     |

#### Repositório do Backend - Financeiro
| Métrica                      | Valor referência | Valor alcançado|
| ---------------------------- | ------------     |----------------|
| Complexity                   | até 10           |     162        |
| Comment Lines Density (%)    | até 30%          |     5,5%       |
| Duplicated Lines Density (%) | até 5%           |     0,0%       |
| Coverage                     | acima de 80%     |     86,5%      |
| Test Failures                | 0                |     0          |
| Test Errors                  | 0                |     0          |
| Security Rating              | 0 (A)            |     0(A)       |
| Satisfação do usuário        | acima de 3       |     |

#### Repositório do Backend - Benefícios
| Métrica                      | Valor referência | Valor alcançado|
| ---------------------------- | ------------     |----------------|
| Complexity                   | até 10           |       28       |
| Comment Lines Density (%)    | até 30%          |       4,7%     |
| Duplicated Lines Density (%) | até 5%           |       0,0%     |
| Coverage                     | acima de 80%     |       70,4%    |
| Test Failures                | 0                |       0        |
| Test Errors                  | 0                |       0        |
| Security Rating              | 0 (A)            |       1(E)     |
| Satisfação do usuário        | acima de 3       |       |


## Histórico de Versões
| Alteração            | Data     | Autor        |
|----------------------|----------|--------------|
| Criação do documento | 28/07/24 | Ingrid Carvalho |
| Atualizações sobre o sonar| 31/08/2024 | Ingrid Carvalho |
| Atualizações com as métricas| 08/09/2024 | Ingrid Carvalho |

## Referências
[ISO/IEC 25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)
