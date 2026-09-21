# Relatório de bugs

## Situação atual

Existe um bug simulado registrado. Ele serve apenas para demonstrar a elaboração
de um relatório de defeito e não foi encontrado em uma aplicação real.

## Estrutura que será utilizada

Cada bug deverá informar:

- identificador;
- título;
- requisito relacionado;
- ambiente;
- pré-condição;
- passos para reprodução;
- resultado esperado;
- resultado obtido;
- severidade;
- prioridade;
- evidência;
- status.

## BUG-001 — Clique duplo cria cadastros duplicados

- **Origem:** defeito simulado.
- **Requisitos relacionados:** CAD-005 e CAD-010.
- **Caso de teste relacionado:** CT-030.
- **Ambiente:** tela de cadastro simulada; sem aplicação funcional.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Severidade:** Alta.
- **Prioridade:** Alta.
- **Evidência:** não disponível, pois a execução é simulada.
- **Status:** Corrigido — reteste simulado aprovado.

### Passos para reprodução

1. Informar `João Silva` no campo Nome.
2. Informar o e-mail `clique.duplo@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar duas vezes rapidamente o botão Cadastrar.

### Resultado esperado

- O botão deve ficar temporariamente desabilitado durante o processamento.
- Apenas um cadastro deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida uma única vez.

### Resultado obtido

O sistema processou as duas solicitações e criou dois cadastros com o mesmo
e-mail.

## BUG-002 — E-mail duplicado é aceito com diferença entre maiúsculas e minúsculas

- **Origem:** defeito simulado.
- **Requisitos relacionados:** EML-003, EML-004 e EML-005.
- **Caso de teste relacionado:** CT-014.
- **Ambiente:** tela de cadastro simulada; sem aplicação funcional.
- **Pré-condição:** o e-mail `andeil@example.com` já pertence a um usuário.
- **Severidade:** Alta.
- **Prioridade:** Alta.
- **Evidência:** não disponível, pois a execução é simulada.
- **Status:** Corrigido — reteste simulado aprovado.

### Passos para reprodução

1. Informar `Maria Silva` no campo Nome.
2. Informar o e-mail `ANDEIL@EXAMPLE.COM`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve considerar o e-mail já cadastrado.
- O novo usuário não deve ser criado.
- A mensagem “E-mail já cadastrado” deve aparecer abaixo do campo E-mail.

### Resultado obtido

O sistema considerou os endereços diferentes por causa das letras maiúsculas e
criou um novo usuário com o mesmo e-mail.

## BUG-003 — Sistema aceita nome acima do limite máximo

- **Origem:** defeito simulado.
- **Requisitos relacionados:** NOM-003 e NOM-007.
- **Caso de teste relacionado:** CT-007.
- **Ambiente:** tela de cadastro simulada; sem aplicação funcional.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Severidade:** Média.
- **Prioridade:** Média.
- **Evidência:** não disponível, pois a execução é simulada.
- **Status:** Corrigido — reteste simulado aprovado.

### Passos para reprodução

1. Preparar e conferir um texto com exatamente 101 letras.
2. Informar esse texto no campo Nome.
3. Informar o e-mail `limite101@example.com`.
4. Informar a senha `Teste seguro 1!`.
5. Sair do campo Nome e observar a validação.
6. Se o botão Cadastrar ficar habilitado, selecioná-lo.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome deve conter entre 2 e 100 caracteres” deve aparecer abaixo
  do campo Nome.
- O botão Cadastrar deve permanecer desabilitado.

### Resultado obtido

O sistema aceitou o nome com 101 caracteres, habilitou o botão Cadastrar e criou
o usuário.
