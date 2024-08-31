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

## Histórico de Versões
| Alteração            | Data     | Autor        |
|----------------------|----------|--------------|
| Criação do documento | 28/07/24 | Ingrid Carvalho |
| Atualizações sobre o sonar| 31/08/2024 | Ingrid Carvalho |

## Referências
[ISO/IEC 25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)
