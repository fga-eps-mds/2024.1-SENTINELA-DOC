---
name: New Issue
about: Template para criação de issues

---

## Nome da issue:
Caso a issue seja uma história de usuário o nome da *issue* deve ser:
- Eu como [tipo de usuário] gostaria de [ação desejada] para [motivo/benefício].

Do contrário:
- O nome da *issue* deve conter uma breve descrição sobre o problema a ser resolvido e deve ser escrito no infinitivo.

### Critérios de aceitação 

#### Interface de cadastro
- [ ] Criação de interface.
- [ ] A interface deve ser responsiva, suportando diferentes tamanhos de tela (desktop, tablet, mobile).
- [ ] Campos obrigatórios: [Lista de campos obrigatórios]
- [ ] Campos opcionais: [Lista de campos opcionais]

#### Validação de campos:
- [ ] Os campos - [Lista de campos de data] - devem estar em formato de data
- [ ] Os campos - [Lista de campos de data] não devem aceitar datas inválidas e não podem aceitar datas no passado exceto em caso de edição
- [ ] O campo [campo de número] deve se adequar a quantidade de caracteres informados
- [ ] O campo [campo de número] não deve aceitar valores não numéricos
- [ ] Exibir uma mensagem de erro "[Erro específico]" se a validação falhar
- [ ] O campo [campo de email] deve seguir o formato de email padrão (e.g., usuario@dominio.com), 
- [ ] O campo [campo de email] deve conter um caractere "@" e um domínio válido (e.g., .com, .org, .net, etc.)
- [ ] Caso o [campo de email] não se encaixe no descrito anteriormente deve exibir uma mensagem de erro "[Erro de email inválido]".
- [ ] O valor inserido para [campo de telefone] deve seguir o formato padrão de números de telefone brasileiros (e.g., (##) ####-#### ou (##) #####-####).
- [ ] Deve aceitar tanto números de telefone fixo (10 dígitos) quanto celular (11 dígitos).
- [ ] Exibir uma mensagem de erro "[Erro de telefone inválido]" se a validação falhar.
- [ ] O campo [campo de URL] deve aceitar somente URL válida (e.g., http://www.exemplo.com/ ou https://www.exemplo.com/).
- [ ] Exibir uma mensagem de erro "[Erro de URL inválida]" se a validação falhar.

#### Funcionalidade de Salvar (ao clicar no botão "Salvar")
- [ ] Todos os campos obrigatórios devem ser validados.
- [ ] Se todas as validações forem passadas, [entidade] deve ser salvo no banco de dados.
- [ ] Exibir uma mensagem de sucesso "[Mensagem de sucesso]".
- [ ] Redirecionar o usuário para [ação após salvar].

#### Deletar [entidade]
- [ ] Exibir uma mensagem de confirmação antes de excluir.
- [ ] Após a confirmação, [entidade] deve ser removido do banco de dados.
- [ ] Exibir uma mensagem de sucesso "[Mensagem de exclusão bem-sucedida]".

#### Atualizar [entidade]
- [ ] Ao acessar a edição, todos os campos devem ser preenchidos com os dados existentes.
- [ ] Após a edição, as mesmas validações e mensagens de sucesso devem ser aplicadas.

#### Listar [entidade]
- [ ] Exibir informações cadastrados - [Campos de exibição]

### Tarefas
- [ ] Especificar critérios de aceitação
- [ ] Criar protótipo da tela 
- [ ] Enviar US e protótipo para validação do cliente
- [ ] Gerar código fonte responsivo conforme protótipo e critérios de aceitação
- [ ] Testes

### Protótipo
[Link para o protótipo]
