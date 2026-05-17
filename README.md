# API de Cadastro de Alunos

## Visão geral
API REST em Node.js com Express para cadastrar alunos em memória.

Arquitetura em camadas:
- Controller
- Routes
- Services
- Models
- Banco de dados em memória

## Endpoints
- `POST /aluno` - cadastra um novo aluno
- `GET /docs` - documentação Swagger UI

## Regras de negócio implementadas
- Campos obrigatórios: `nome`, `cpf`, `email`, `telefone`
- Validações de tipo mínimo: `nome` e `email` strings, `cpf` e `telefone` numéricos
- CPF único (retorna 409 se já cadastrado)
- Retorna 400 para entrada inválida

## Execução
1. Instalar dependências

```bash
npm install
```

2. Iniciar API

```bash
npm start
```

3. Acessar Swagger UI

http://localhost:3000/docs

## Testes
Executar:

```bash
npm test
```

## Estrutura de pastas
- `.src` - código fonte
- `.test` - testes automatizados
- `resources` - Swagger
- `tests/fixtures` - fixtures de teste
