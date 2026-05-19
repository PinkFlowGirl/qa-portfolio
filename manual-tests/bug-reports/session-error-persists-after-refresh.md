# 🐞 Bug Report

## Título
Mensagem de erro persiste após refresh mesmo com usuário autenticado

---

## Ambiente
- Navegador: Chrome
- Sistema Operacional: Windows 11

---

## Passos para reproduzir
1. Fazer login no Sauce Demo
2. Abrir detalhes de um produto
3. Voltar utilizando o navegador
4. Observar mensagem de erro exibida
5. Atualizar a página utilizando refresh

---

## Resultado esperado
Sistema deve manter estado consistente da sessão ou redirecionar corretamente sem persistir mensagem de erro.

---

## Resultado atual
Mensagem:
"You can only access '/inventory-item.html' when you are logged in."
permanece exibida mesmo após refresh da página com usuário autenticado.

---

## Severidade
Média

---

## Prioridade
Média

---

## Tipo
Funcional / Sessão / UX