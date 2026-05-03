# Relatório de Bugs — SauceDemo

## Resumo

Durante a execução dos testes manuais no SauceDemo, foi identificado 1 bug no fluxo de finalização de compra.

---

## Bug 001 — Erro ao finalizar compra no checkout

**ID:** BUG-001

**Título:** Sistema redireciona para a tela de login ao finalizar compra, mesmo com usuário autenticado no checkout.

**Caso de teste relacionado:** CT-013 — Finalizar compra

**Descrição:**  
Ao executar a etapa final do checkout e clicar no botão **Finish**, o sistema não concluiu a compra conforme esperado. Em vez disso, retornou para a tela de login e exibiu uma mensagem informando que o checkout só pode ser acessado com uma conta autenticada, embora o fluxo já estivesse sendo executado com uma conta logada.

**Pré-condição:**  
Usuário autenticado no sistema e posicionado na etapa final do checkout.

**Passos para reproduzir:**

1. Acessar o site SauceDemo
2. Realizar login com usuário válido
3. Adicionar um produto ao carrinho
4. Acessar o carrinho
5. Clicar em Checkout
6. Preencher os dados obrigatórios
7. Avançar até a tela de resumo da compra
8. Clicar em Finish

**Resultado esperado:**  
O sistema deve concluir a compra e exibir a mensagem de sucesso.

**Resultado obtido:**  
O sistema retornou para a tela de login e exibiu mensagem de erro informando que somente usuários autenticados podem acessar o checkout.

**Severidade:** Alta

**Prioridade:** Alta

**Status:** Aberto

**Impacto:**  
O bug impede a conclusão do fluxo principal de compra do sistema.

**Evidência:**  
`evidencias/CT-013-compra-finalizada-bug.png`