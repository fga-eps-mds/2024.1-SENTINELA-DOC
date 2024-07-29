# Arquitetura de Software

### Visão Geral

A arquitetura deste sistema é composta por uma interface central que se comunica com três microsserviços distintos: Usuários, Financeiro e Benefícios.

Os microsserviços são responsáveis por áreas funcionais específicas e se comunicam de forma assíncrona e segura através de APIs. Cada microsserviço expõe uma interface de API que permite que a interface central e os outros microsserviços realizem operações conforme necessário.

A separação dos microsserviços e seus bancos de dados permite a escalabilidade independente de cada componente. Alterações e manutenções em um microsserviço não afetam diretamente os outros, promovendo uma arquitetura facilmente adaptável a mudanças.

### Componentes da Arquitetura

#### 1. **Interface**

A interface atua como o ponto de entrada para os usuários e sistemas externos, permitindo a interação com o sistema de forma integrada. Esta camada é responsável por:

- **Recepção de Requisições**: Captura e valida as requisições dos usuários ou sistemas externos.
- **Autenticação e Autorização**: Garante que as requisições sejam realizadas por usuários autorizados e autenticados.
- **Orquestração de Requisições**: Coordena as interações entre os microsserviços, garantindo que as respostas sejam consolidadas e apresentadas ao usuário final de forma coesa.

#### 2. **Microsserviço de Usuários**

O microsserviço de Usuários gerencia todas as operações relacionadas aos usuários do sistema.

**Banco de Dados do Usuários**: O banco de dados associado a este microsserviço armazena informações detalhadas sobre cada usuário

#### 3. **Microsserviço Financeiro**

O microsserviço Financeiro é responsável por gerenciar todas as transações e operações financeiras.
**Banco de Dados do Financeiro**: O banco de dados deste microsserviço armazena dados relacionados a fornecedores, contas e históricos financeiros.

#### 4. **Microsserviço de Benefícios**

O microsserviço de Benefícios cuida da administração dos benefícios/convênios oferecidos aos sindicalizados.
**Banco de Dados de Benefícios**: O banco de dados deste microsserviço armazena informações sobre os benefícios disponíveis.

![Representacao da arquietura](./assets/arq.png)

## Histórico de Versão

| Alteração            | Data     | Autor       |
| -------------------- | -------- | ----------- |
| Criação do documento | 28/07/24 | Sara Campos |
