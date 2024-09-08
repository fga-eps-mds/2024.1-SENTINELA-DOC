# Integração e deploy contínuos

## CD

Considerando a arquitetura do sistema organizada em microsserviços foi necessário que o deploy seguisse essa mesma arquitetura. Dessa forma foram utilizadas 3 diferentes plataformas para hospedagem de cada etapa dos sistema.
Primeiramente foi escolhida a plataforma netlify para a hospedagem do frontend do sistema. A plataforma é simlpes e intuitiva e já permite a conexão com deploy contínuo de branches específicas, permitindo a criação de um ambiente de homologação das histórias.
Para os backends, seu deploy foi separado dos respectivos bancos de dados, visto que a plataforma Render não permitia a hospedagem desses mesmos de forma gratuita. Assim foram criados 3 instâncias separadas no render, contendo cada um dos backends utilizados, Usuários, Financeiro e Benefícios. Por fim, os bancos de dados foram hospedados no Mongo Atlas, permitindo maior facilidade de acesso ao banco diretamente para verificar possíveis inconsistências sem necessidade de custos adicionais.
A conexão entre o frontend e o back foi feita pela utilização de variáveis de ambiente fácilmente configuráveis para endereçar os endpoints necessários. De forma similar foi feita a conexão de cada um dos backend com seu respectivo banco de dados.

## Histórico de Versões

| Alteração            | Data     | Autor                                        |
| -------------------- | -------- | -------------------------------------------- |
| Criação do documento | 08/09/24 | Ingrid Carvalho, Alvaro Gouvea e Sara Campos |
