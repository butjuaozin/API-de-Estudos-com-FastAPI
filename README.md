# API-de-Estudos-com-FastAPI
## 📖 Sobre o projeto

Esta API permite **listar** e **cadastrar** alunos em uma lista em memória (sem banco de dados real). O projeto também serviu para praticar rotas com parâmetros, validação de dados com Pydantic e tratamento de erros com `HTTPException`.

> ⚠️ Os dados ficam na memória: ao reiniciar o servidor, tudo volta ao estado inicial.

## 💡 Inspiração

Quis entender como aplicativos e sites conversam com um servidor por trás dos panos. O FastAPI chamou minha atenção por ser simples para iniciantes e por gerar a documentação da API automaticamente.

## 🛠️ Tecnologias utilizadas

- Python 3
- [FastAPI](https://fastapi.tiangolo.com/)
- [Pydantic](https://docs.pydantic.dev/) (validação de dados)
- [Uvicorn](https://www.uvicorn.org/) (servidor)

## ▶️ Como usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU-USUARIO/api-fastapi-estudos.git
   cd api-fastapi-estudos
   ```
2. Instale as dependências:
   ```bash
   pip install fastapi "uvicorn[standard]"
   ```
3. Rode o servidor:
   ```bash
   uvicorn main:app --reload
   ```
4. Abra no navegador:
   - Swagger UI (testar as rotas): http://127.0.0.1:8000/docs
   - ReDoc (documentação): http://127.0.0.1:8000/redoc

## 📌 Endpoints

| Método | Rota      | Descrição                  | Retorno |
|--------|-----------|----------------------------|---------|
| GET    | `/banco/` | Lista todos os alunos      | 200     |
| POST   | `/banco/` | Cadastra um novo aluno     | 201     |

### Exemplo de cadastro (POST `/banco/`)

Corpo da requisição:
```json
{
  "id": 2,
  "nome": "Maria"
}
```

Resposta:
```json
{
  "mensagem": "Cadastrado com sucesso",
  "aluno": {
    "id": 2,
    "nome": "Maria"
  }
}
```

## ✨ O que aprendi

- O que é uma API e como funcionam as rotas (GET e POST)
- Parâmetros de rota e de consulta (`skip` e `limit`)
- Validação de dados com modelos Pydantic
- Códigos de status HTTP (200, 201, 404)
- Tratamento de erros com `HTTPException`
- Documentação automática com Swagger UI e OpenAPI

## 🔮 Próximos passos

- Adicionar rotas de atualizar (PUT) e remover (DELETE)
- Impedir cadastro de alunos com `id` repetido
- Conectar a um banco de dados real

## 👨‍💻 Autor

**João Eduardo**
Estudante de programação
[GitHub](https://github.com/butjuaozin)
