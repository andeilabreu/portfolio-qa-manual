# Resultado dos testes

## Situação atual

Este projeto não possui uma aplicação funcional. Por isso, os resultados desta
etapa são **simulados** e servem apenas para demonstrar o processo de execução
de testes e registro de defeitos.

## Resumo

- Casos documentados: 34.
- Casos executados: 34.
- Casos aprovados: 31.
- Casos reprovados: 3.
- Casos não executados: 0.

## Execuções registradas

- **CT-030 — Clique duplo no botão Cadastrar**
  - Resultado simulado: o sistema criou dois cadastros com o mesmo e-mail.
  - Status: Reprovado.
  - Bug relacionado: BUG-001.
- **CT-014 — E-mail duplicado com letras maiúsculas**
  - Resultado simulado: o sistema criou outro usuário porque tratou letras
    maiúsculas e minúsculas como diferentes.
  - Status: Reprovado.
  - Bug relacionado: BUG-002.
- **CT-007 — Nome com 101 caracteres**
  - Resultado simulado: o sistema aceitou o nome acima do limite máximo e criou
    o usuário.
  - Status: Reprovado.
  - Bug relacionado: BUG-003.
- **CT-003 — Nome com 2 caracteres**
  - Resultado simulado: o sistema aceitou o nome no limite mínimo, criou o
    usuário e exibiu a mensagem de sucesso.
  - Status: Aprovado.
- **CT-016 — Senha com 12 caracteres**
  - Resultado simulado: o sistema aceitou a senha no limite mínimo, criou o
    usuário e exibiu a mensagem de sucesso.
  - Status: Aprovado.
- **CT-019 — Senha com 64 caracteres**
  - Resultado simulado: o sistema aceitou a senha no limite máximo, criou o
    usuário e exibiu a mensagem de sucesso.
  - Status: Aprovado.

## Demais casos aprovados

Os outros 28 casos apresentaram, na simulação, comportamento correspondente ao
resultado esperado e foram classificados como **Aprovados**. Os resultados
individuais estão registrados em `casos-de-teste.md`.

## Observação

Os resultados simulados serão sempre identificados claramente para não serem
confundidos com testes realizados em uma aplicação real.

## Reteste e regressão

Os três bugs receberam correções simuladas. Os três retestes e os três casos de
regressão foram aprovados. Os detalhes estão em `reteste-e-regressao.md`.
