# Casos de teste — Cadastro de usuário

## Orientação

Cada caso de teste deve estar ligado a um requisito. Os dados deste projeto são
fictícios e o sistema é simulado.

Como não existe uma aplicação para executar neste momento, os casos permanecerão
com o status **Não executado**.

## CT-001 — Cadastro com o campo Nome vazio

- **Requisito relacionado:** NOM-001 e NOM-006.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema impede o cadastro quando o Nome não é
  informado.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: vazio;
  - E-mail: `andeil.teste@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Deixar o campo Nome vazio.
2. Informar o e-mail `andeil.teste@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome é obrigatório” deve aparecer abaixo do campo Nome.
- O campo Nome deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-002 — Nome com 1 caractere

- **Requisitos relacionados:** NOM-002 e NOM-007.
- **Tipo de teste:** negativo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente abaixo do tamanho
  mínimo aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `A`;
  - E-mail: `limite1@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `A` no campo Nome.
2. Informar o e-mail `limite1@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome deve conter entre 2 e 100 caracteres” deve aparecer abaixo
  do campo Nome.
- O campo Nome deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-003 — Nome com 2 caracteres

- **Requisito relacionado:** NOM-002.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o tamanho mínimo aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Al`;
  - E-mail: `limite2@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Al` no campo Nome.
2. Informar o e-mail `limite2@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-004 — Nome com 3 caracteres

- **Requisito relacionado:** NOM-002.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente acima do tamanho mínimo
  aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Ana`;
  - E-mail: `limite3@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Ana` no campo Nome.
2. Informar o e-mail `limite3@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-005 — Nome com 99 caracteres

- **Requisito relacionado:** NOM-003.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente abaixo do tamanho
  máximo aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: texto formado por exatamente 99 letras;
  - E-mail: `limite99@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Preparar e conferir um texto com exatamente 99 letras.
2. Informar esse texto no campo Nome.
3. Informar o e-mail `limite99@example.com`.
4. Informar a senha `Teste seguro 1!`.
5. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-006 — Nome com 100 caracteres

- **Requisito relacionado:** NOM-003.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o tamanho máximo aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: texto formado por exatamente 100 letras;
  - E-mail: `limite100@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Preparar e conferir um texto com exatamente 100 letras.
2. Informar esse texto no campo Nome.
3. Informar o e-mail `limite100@example.com`.
4. Informar a senha `Teste seguro 1!`.
5. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-007 — Nome com 101 caracteres

- **Requisitos relacionados:** NOM-003 e NOM-007.
- **Tipo de teste:** negativo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente acima do tamanho máximo
  aceito para o Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: texto formado por exatamente 101 letras;
  - E-mail: `limite101@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Preparar e conferir um texto com exatamente 101 letras.
2. Informar esse texto no campo Nome.
3. Informar o e-mail `limite101@example.com`.
4. Informar a senha `Teste seguro 1!`.
5. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome deve conter entre 2 e 100 caracteres” deve aparecer abaixo
  do campo Nome.
- O campo Nome deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-008 — Nome contendo números

- **Requisito relacionado:** NOM-005.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema rejeita números no campo Nome.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil123`;
  - E-mail: `numeros.nome@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Andeil123` no campo Nome.
2. Informar o e-mail `numeros.nome@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome contém caracteres não permitidos. Use letras, espaços,
  hífen ou apóstrofo” deve aparecer abaixo do campo Nome.
- O campo Nome deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-009 — Nomes com caracteres permitidos

- **Requisito relacionado:** NOM-004.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o campo Nome aceita hífen, apóstrofo, espaços e
  letras acentuadas.
- **Pré-condição:** usuário está na tela de cadastro e os e-mails de teste ainda
  não foram utilizados.
- **Dados de teste:**
  - `Ana-Maria` com o e-mail `ana.maria@example.com`;
  - `D'Ávila` com o e-mail `davila@example.com`;
  - `João da Silva` com o e-mail `joao.silva@example.com`;
  - Senha para todos os testes: `Teste seguro 1!`.

### Passos

Executar os passos abaixo separadamente para cada nome e e-mail:

1. Informar o Nome.
2. Informar o E-mail correspondente.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- Cada nome deve ser aceito.
- Cada usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-010 — E-mails com formato inválido

- **Requisito relacionado:** EML-002.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema rejeita e-mails sem a estrutura básica
  completa.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - `andeil.com`;
  - `@dominio.com`;
  - `andeil@`;
  - Nome para todos os testes: `Andeil Abreu`;
  - Senha para todos os testes: `Teste seguro 1!`.

### Passos

Executar os passos abaixo separadamente para cada e-mail:

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o E-mail inválido.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-011 — E-mail com formato válido

- **Requisito relacionado:** EML-002.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se um endereço com a estrutura básica completa é
  aceito.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `andeil@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `andeil@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-012 — Campo E-mail vazio

- **Requisito relacionado:** EML-001.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema impede o cadastro quando o E-mail não é
  informado.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: vazio;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Deixar o campo E-mail vazio.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-013 — E-mail já cadastrado

- **Requisitos relacionados:** EML-003 e EML-005.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema bloqueia um segundo cadastro com um
  e-mail já utilizado.
- **Pré-condição:** o e-mail `andeil@example.com` já pertence a um usuário.
- **Dados de teste:**
  - Nome: `Maria Silva`;
  - E-mail: `andeil@example.com`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Maria Silva` no campo Nome.
2. Informar o e-mail `andeil@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O novo usuário não deve ser criado.
- A mensagem “E-mail já cadastrado” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-014 — E-mail duplicado com letras maiúsculas

- **Requisitos relacionados:** EML-003, EML-004 e EML-005.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se a validação de duplicidade ignora diferenças entre
  letras maiúsculas e minúsculas.
- **Pré-condição:** o e-mail `andeil@example.com` já pertence a um usuário.
- **Dados de teste:**
  - Nome: `Maria Silva`;
  - E-mail: `ANDEIL@EXAMPLE.COM`;
  - Senha: `Teste seguro 1!`.

### Passos

1. Informar `Maria Silva` no campo Nome.
2. Informar o e-mail `ANDEIL@EXAMPLE.COM`.
3. Informar a senha `Teste seguro 1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve considerar o e-mail já cadastrado.
- O novo usuário não deve ser criado.
- A mensagem “E-mail já cadastrado” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-015 — Senha com 11 caracteres

- **Requisito relacionado:** SEN-002.
- **Tipo de teste:** negativo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente abaixo do tamanho
  mínimo aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha11@example.com`;
  - Senha: `Senha 12345`, com 11 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha11@example.com`.
3. Informar a senha `Senha 12345`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “A senha deve conter no mínimo 12 caracteres” deve aparecer abaixo
  do campo Senha.
- O campo Senha deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-016 — Senha com 12 caracteres

- **Requisito relacionado:** SEN-002.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o tamanho mínimo aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha12@example.com`;
  - Senha: `Senha 123456`, com 12 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha12@example.com`.
3. Informar a senha `Senha 123456`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-017 — Senha com 13 caracteres

- **Requisito relacionado:** SEN-002.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente acima do tamanho mínimo
  aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha13@example.com`;
  - Senha: `Senha 1234567`, com 13 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha13@example.com`.
3. Informar a senha `Senha 1234567`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-018 — Senha com 63 caracteres

- **Requisito relacionado:** SEN-003.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente abaixo do tamanho
  máximo aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha63@example.com`;
  - Senha: texto formado por exatamente 63 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha63@example.com`.
3. Preparar, conferir e informar uma senha com exatamente 63 caracteres.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-019 — Senha com 64 caracteres

- **Requisito relacionado:** SEN-003.
- **Tipo de teste:** positivo e valor-limite.
- **Objetivo:** verificar o tamanho máximo aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha64@example.com`;
  - Senha: texto formado por exatamente 64 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha64@example.com`.
3. Preparar, conferir e informar uma senha com exatamente 64 caracteres.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-020 — Senha com 65 caracteres

- **Requisito relacionado:** SEN-003.
- **Tipo de teste:** negativo e valor-limite.
- **Objetivo:** verificar o comportamento imediatamente acima do tamanho máximo
  aceito para a Senha.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha65@example.com`;
  - Senha: texto formado por exatamente 65 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha65@example.com`.
3. Preparar, conferir e informar uma senha com exatamente 65 caracteres.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “A senha deve conter no máximo 64 caracteres” deve aparecer abaixo
  do campo Senha.
- O campo Senha deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.

## CT-021 — Campo Senha vazio

- **Requisito relacionado:** SEN-001.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema impede o cadastro quando a Senha não é
  informada.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha.vazia@example.com`;
  - Senha: vazia.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha.vazia@example.com`.
3. Deixar o campo Senha vazio.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Senha é obrigatória” deve aparecer abaixo do campo Senha.
- O campo Senha deve ficar destacado.

### Execução

- **Resultado obtido:** não executado.
- **Status:** Não executado.
