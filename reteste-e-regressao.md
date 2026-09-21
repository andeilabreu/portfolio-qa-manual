# Reteste e regressão

## Situação

Esta etapa é simulada, pois o projeto não possui uma aplicação funcional. Foi
considerado que os três bugs registrados receberam correções simuladas e estão
disponíveis para reteste.

## Objetivo

- **Reteste:** confirmar se a correção resolveu o bug específico.
- **Regressão:** verificar se a correção não prejudicou outras funcionalidades
  que já funcionavam.

## Retestes planejados

### RT-001 — Impedir cadastro duplicado por clique duplo

- **Bug relacionado:** BUG-001.
- **Caso de teste original:** CT-030.
- **Resultado esperado:** apenas um cadastro deve ser criado quando o botão for
  selecionado duas vezes rapidamente.
- **Resultado obtido (simulado):** após a correção, dois cliques rápidos
  resultaram em apenas um cadastro e uma mensagem de sucesso.
- **Status:** Aprovado.

### RT-002 — Identificar e-mail duplicado sem diferenciar maiúsculas e minúsculas

- **Bug relacionado:** BUG-002.
- **Caso de teste original:** CT-014.
- **Resultado esperado:** `andeil@example.com` e `ANDEIL@EXAMPLE.COM` devem ser
  considerados o mesmo endereço, impedindo o segundo cadastro.
- **Resultado obtido (simulado):** após a correção, o sistema reconheceu os
  dois endereços como o mesmo e-mail, impediu o segundo cadastro e exibiu
  “E-mail já cadastrado”.
- **Status:** Aprovado.

### RT-003 — Recusar nome com 101 caracteres

- **Bug relacionado:** BUG-003.
- **Caso de teste original:** CT-007.
- **Resultado esperado:** o sistema deve recusar o nome acima de 100 caracteres
  e manter o botão Cadastrar desabilitado.
- **Resultado obtido (simulado):** após a correção, o sistema recusou o nome
  com 101 caracteres, exibiu a mensagem esperada e manteve o botão Cadastrar
  desabilitado.
- **Status:** Aprovado.

## Regressão

Após os retestes, foram repetidos casos relacionados para verificar se as
correções não prejudicaram comportamentos que já funcionavam.

### RG-001 — Cadastro com nome no limite máximo

- **Caso de teste utilizado:** CT-006.
- **Motivo:** confirmar que a correção do limite de 101 caracteres não passou a
  recusar o valor válido de 100 caracteres.
- **Resultado obtido (simulado):** o nome com 100 caracteres foi aceito e o
  cadastro foi realizado.
- **Status:** Aprovado.

### RG-002 — Bloqueio de e-mail duplicado idêntico

- **Caso de teste utilizado:** CT-013.
- **Motivo:** confirmar que a correção da comparação entre maiúsculas e
  minúsculas manteve o bloqueio de um endereço exatamente igual.
- **Resultado obtido (simulado):** o segundo cadastro foi impedido e a mensagem
  “E-mail já cadastrado” foi exibida.
- **Status:** Aprovado.

### RG-003 — Cadastro com dados válidos

- **Caso de teste utilizado:** CT-011.
- **Motivo:** confirmar que as correções não impediram um cadastro comum com
  dados válidos.
- **Resultado obtido (simulado):** o usuário foi criado uma única vez e a
  mensagem de sucesso foi exibida.
- **Status:** Aprovado.

## Resumo

- Retestes executados: 3.
- Retestes aprovados: 3.
- Casos de regressão executados: 3.
- Casos de regressão aprovados: 3.
- Bugs que permaneceram abertos após o reteste: 0.
