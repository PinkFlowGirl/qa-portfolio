# Casos de Teste — Kpop Events Finder API

## Ambiente
- URL: http://localhost:3000
- Documentação: http://localhost:3000/api-docs
- Ferramenta: Swagger / Postman

---

## GET /health

| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-001 | Health check com sucesso | GET /health | 200 + body com status "ok" | ✅ Pass |
| TC-002 | Endpoint com typo | GET /healt | 404 Not Found | ✅ Pass |
| TC-003 | Método errado | POST /health | 405 Method Not Allowed | ⚠️ Retornou 404 — ponto de atenção para o time |

---

## POST /api/v1/auth/register
| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-004 | Registro com sucesso | 201 + id, name, email, createdAt, updatedAt, token | ✅ Pass |
| TC-005 | Email já cadastrado | 409 Conflict | ✅ Pass |
| TC-006 | Campos obrigatórios em branco | 400 + mensagem explicativa | ✅ Pass |

---

## POST /api/v1/auth/login
| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-007 | Login com sucesso | POST com email e senha válidos | 200 + token JWT | 🔲 A executar |
| TC-008 | Senha incorreta | POST com senha errada | 401 Unauthorized | 🔲 A executar |
| TC-009 | Email não cadastrado | POST com email inexistente | 401 Unauthorized | 🔲 A executar |

---

## GET /api/v1/auth/me
| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-010 | Buscar perfil autenticado | GET com token válido | 200 + dados do usuário | 🔲 A executar |
| TC-011 | Buscar perfil sem token | GET sem token | 401 Unauthorized | 🔲 A executar |

---

## POST /api/v1/events
| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-012 | Criar evento com sucesso | POST com dados válidos e token | 201 Created | 🔲 A executar |
| TC-013 | Criar evento sem autenticação | POST sem token | 401 Unauthorized | 🔲 A executar |
| TC-014 | Criar evento sem campos obrigatórios | POST sem body | 400 Bad Request | 🔲 A executar |

---

## GET /api/v1/events
| ID | Cenário | Passos | Resultado Esperado | Status |
|---|---|---|---|---|
| TC-015 | Listar eventos com sucesso | GET com token válido | 200 + lista de eventos | 🔲 A executar |
| TC-016 | Listar eventos sem autenticação | GET sem token | 401 Unauthorized | 🔲 A executar |