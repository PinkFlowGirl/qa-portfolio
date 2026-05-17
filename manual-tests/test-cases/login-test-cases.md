# Test Cases - Login

| ID | Cenário | Passos | Resultado Esperado |
|---|---|---|---|
| CT-01 | Login válido | Inserir usuário standard_user e senha secret_sauce | Usuário acessa a página de produtos |
| CT-02 | Senha inválida | Inserir usuário válido e senha incorreta | Sistema exibe mensagem de erro |
| CT-03 | Usuário inválido | Inserir usuário inexistente | Sistema exibe mensagem de erro |
| CT-04 | Campos vazios | Clicar em Login sem preencher os campos | Sistema informa que os campos são obrigatórios |
| CT-05 | Apenas senha preenchida | Inserir apenas senha e clicar em Login | Sistema informa que o usuário é obrigatório |