# Melhorias e defeitos identificados no projeto

Ao longo do desenvolvimento, foram identificadas evoluções corretivas e adaptativas, bem como bugs de funcionamento, todos apresentados neste documento.

A qualidade de entrega sempre foi considerada como essencial para o time, de forma que, sempre que algum integrante identificava alguma oportunidade de adaptação ou correção no produto, antes ou depois da aceitação por parte dos P.Os, o encaminhamento era feito.

Assim, foram adicionadas issues de _Enhancement_ relacionadas às US que apresentavam essa necessidade. No total, foram instanciadas três melhorias, das quais duas foram conduzidas e entregues aos P.Os.

| ENH  | US   | Descrição                                                                                                                                                                                                                   | Entrega        |
| ---- | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| #105 | US02 | Evolução adaptativa da US02 (Solicitar filiação), que implica na necessidade dos campos Sexo, Lotação, Órgão e Situação Atual se tornarem obrigatórios e os campos Órgão e Lotação devem se tornam campos do tipo Dropdown. | Entregue       |
| #108 | US05 | Evolução corretiva que apresente feedback para o usuário ao alterar o nome de conta bancária para string vazia                                                                                                              | Entregue       |
| #106 | US04 | Ajuste do banco de dados, de forma que, a tabela de sindicalizados seja filha da tabela usuários (herança) e reflexo disso no frontend, ou seja, exibição dos dados na tela conforme tipo de usuário.                       | Não finalizada |

Além disso, foi instanciada a necessidade de duas novas US no Backlog do Produto, das quais uma foi trazida para desenvolvimento nesse semestre, devido a sua prioridade (US35 - Cadastrar órgãos/lotações), e a outra foi identificada para ser desenvolvida futuramente, em outros semestres (US36 - Cadastrar postos de trabalho).

A não finalização da US04, assim como a não entrega da ENH-US04 implicam na necessidade de revisão e refatoramento dos formulários referentes a filiação e cadastro de usuários do tipo filiado, o que deve ser conduzido futuramente pelos próximos times responsáveis.

Com relação a defeitos, alguns foram identificados ao longo do projeto conforme retorno do usuário nos testes de aceitação. Todos estes pedidos foram encaminhados para correção e entregues de acordo, permitindo assim a entrega final das US.

Nas semanas finais (Release N), quando o foco era na entrega de melhorias e correções, o time criou um [Mapeamento de Bugs](https://docs.google.com/spreadsheets/d/1mJo4xZpqivDqr3B99fJFf-j5_3BPYpoKceONAV9nmyE/edit?usp=sharing) a serem corrigidos, bem como foram inspecionados minuciosamente os estilos (CSS/HTML) de algumas páginas para garantir uma boa Experiência de Usuário. Foram elas:

- contributionHistoric [feito]
- fornecedores (create and update) [feito]
- list roles page [feito]
- list user [feito]
- profile (update) [feito]

Por fim, o projeto é finalizado com a necessidade das seguintes correções de defeitos:

| US   | Defeito                                                                                                                                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                 | Prioridade                                                                                                                                         |
| ---- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| US04 | Inicialmente, havia sido levantado que as telas de cadastro de usuários teriam os dados pedidos pelos P.Os. No entanto, enquanto era desenvolvida, notou-se que essa US precisava de telas para representar usuários do tipo filiados. Essa correção, no entanto, não foi finalizada a nível de interface. | A correção foi feita apenas a nível de banco de dados, já que agora as tabelas Usuário e Filiado possuem relação de herança, mas é preciso criar protótipos de como essas telas irão funcionar com a mudança e refletir isso no frontend. | A prioridade dessa correção é considerada alta, pois afeta a performance de outras US e é uma funcionalidade básica do sistema.                    |
| US34 | Quando uma solicitação é rejeitada, um email deve ser enviado ao solicitante para que ele seja informado sobre a rejeição e, caso queira, entre em contato com o sindicato                                                                                                                                 | Esse defeito deve ser corrigido com uma revisão simples do código, visto que, a funcionalidade foi implementada e já havia sido testada antes, mas no momento do teste de aceitação final do usuário acabou não funcionando perfeitamente | A prioridade dessa correção não é tão alta por não afetar outras US, mas por ser uma correção rápida pode ser significativamente priorizada.       |
| US20 | Campo de data com formato MM/DD/YYYY                                                                                                                                                                                                                                                                       | Cadastros antigos feitos antes de uma correção em relação a data ainda exibem formato MM/DD/YY, ao contrário de DD/MM/YYYY, como era esperado, apesar deste problema não ser mais gerável pelos cadastros do usuário                      | Baixa prioridade, não afeta outras US                                                                                                              |
| US20 | Campo de Conta Origem/Destino não recebe contas bancárias cadastradas                                                                                                                                                                                                                                      | Quando selecionada a opção de Conta do Sindicato, as contas bancárias que aparecem como opção de preenchimento são estáticas                                                                                                              | Prioridade alta, porém de baixa complexidade, já que basta uma correção, implementando a requisição GET de Contas Bancárias registradas no sistema |
| US21 | Desfazer selção de filtro                                                                                                                                                                                                                                                                                  | É possível limpar todos os filtros, no entanto, o P.O fez a sugestão de implementar a limpar um filtro por vez                                                                                                                            | Prioridade a ser avaliada pelo P.O                                                                                                                 |

## Histórico de versão

| Alteração                                                             | Data     | Autor       |
| --------------------------------------------------------------------- | -------- | ----------- |
| Criação do documento                                                  | 08/09/24 | Sara Campos |
| Atualização a partir do feedback do P.O (Adiciona tabela de Defeitos) | 09/09/24 | Sara Campos |
| Atualização a partir do feedback do P.O (Adiciona tabela de Defeitos) | 14/09/24 | Sara Campos |
