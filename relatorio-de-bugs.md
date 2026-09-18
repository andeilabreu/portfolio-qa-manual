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
- **Severidade:** a definir.
- **Prioridade:** a definir.
- **Evidência:** não disponível, pois a execução é simulada.
- **Status:** Aberto — simulado.

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
