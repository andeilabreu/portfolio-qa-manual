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

1. Selecionar o campo Nome e sair dele sem preenchê-lo.
2. Informar o e-mail `andeil.teste@example.com`.
3. Informar a senha `Teste seguro 1!`.
4. Observar o estado do botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome é obrigatório” deve aparecer abaixo do campo Nome.
- O campo Nome deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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
2. Sair do campo Nome.
3. Informar o e-mail `limite1@example.com`.
4. Informar a senha `Teste seguro 1!`.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome deve conter entre 2 e 100 caracteres” deve aparecer abaixo
  do campo Nome.
- O campo Nome deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** o sistema aceitou o nome `Al`, criou o
  usuário e exibiu a mensagem “Cadastro realizado com sucesso”.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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
3. Sair do campo Nome.
4. Informar o e-mail `limite101@example.com`.
5. Informar a senha `Teste seguro 1!`.
6. Se o botão Cadastrar ficar habilitado, selecioná-lo.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome deve conter entre 2 e 100 caracteres” deve aparecer abaixo
  do campo Nome.
- O campo Nome deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** o sistema aceitou o nome com 101 caracteres,
  habilitou o botão Cadastrar e criou o usuário.
- **Status:** Reprovado.
- **Bug relacionado:** BUG-003.

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
2. Sair do campo Nome.
3. Informar o e-mail `numeros.nome@example.com`.
4. Informar a senha `Teste seguro 1!`.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome contém caracteres não permitidos. Use letras, espaços,
  hífen ou apóstrofo” deve aparecer abaixo do campo Nome.
- O campo Nome deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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
3. Sair do campo E-mail.
4. Informar a senha `Teste seguro 1!`.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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
2. Selecionar o campo E-mail e sair dele sem preenchê-lo.
3. Informar a senha `Teste seguro 1!`.
4. Observar o estado do botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** o sistema tratou
  `ANDEIL@EXAMPLE.COM` como diferente de `andeil@example.com` e criou um novo
  usuário.
- **Status:** Reprovado.
- **Bug relacionado:** BUG-002.

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
4. Sair do campo Senha.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “A senha deve conter no mínimo 12 caracteres” deve aparecer abaixo
  do campo Senha.
- O campo Senha deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** o sistema aceitou a senha com 12 caracteres,
  criou o usuário e exibiu a mensagem “Cadastro realizado com sucesso”.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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

- **Resultado obtido (simulado):** o sistema aceitou a senha com 64 caracteres,
  criou o usuário e exibiu a mensagem “Cadastro realizado com sucesso”.
- **Status:** Aprovado.

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
4. Sair do campo Senha.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “A senha deve conter no máximo 64 caracteres” deve aparecer abaixo
  do campo Senha.
- O campo Senha deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

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
3. Selecionar o campo Senha e sair dele sem preenchê-lo.
4. Observar o estado do botão Cadastrar.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Senha é obrigatória” deve aparecer abaixo do campo Senha.
- O campo Senha deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-022 — Senha com espaços e símbolos

- **Requisitos relacionados:** SEN-004, SEN-005 e SEN-006.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o sistema aceita uma senha válida contendo letras,
  números, espaços e símbolos, sem alterar os caracteres informados.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `Andeil Abreu`;
  - E-mail: `senha.simbolos@example.com`;
  - Senha: `QA manual #1!`, com 12 caracteres.

### Passos

1. Informar `Andeil Abreu` no campo Nome.
2. Informar o e-mail `senha.simbolos@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve manter a senha exatamente como foi digitada.
- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Nenhuma mensagem de erro deve ser apresentada.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-023 — Senha oculta por padrão

- **Requisito relacionado:** SEN-007.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se os caracteres da senha ficam ocultos por padrão
  durante a digitação.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Senha: `QA manual #1!`.

### Passos

1. Selecionar o campo Senha.
2. Informar a senha `QA manual #1!`.
3. Observar a apresentação dos caracteres durante e após a digitação.

### Resultado esperado

- Os caracteres informados não devem ficar visíveis.
- Cada caractere deve ser representado por um símbolo de ocultação.
- A senha armazenada no campo não deve ser alterada.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-024 — Mostrar e ocultar a senha

- **Requisito relacionado:** SEN-008.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o botão de visibilidade mostra a senha e permite
  ocultá-la novamente sem alterar seu conteúdo.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Senha: `QA manual #1!`.

### Passos

1. Informar a senha `QA manual #1!`.
2. Selecionar o botão para mostrar a senha.
3. Conferir o conteúdo apresentado no campo.
4. Selecionar novamente o botão para ocultar a senha.

### Resultado esperado

- Após o primeiro acionamento, a senha completa deve ficar visível.
- Após o segundo acionamento, a senha deve ficar novamente oculta.
- O conteúdo da senha não deve ser alterado durante essas ações.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-025 — Nome com dois espaços internos

- **Requisito relacionado:** ESP-003.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o sistema reduz espaços internos consecutivos no
  Nome para um único espaço.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `João  Silva`, com dois espaços entre as partes do nome;
  - E-mail: `joao.silva@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João  Silva` no campo Nome.
2. Informar o e-mail `joao.silva@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve reduzir os dois espaços internos para um.
- O nome deve ser registrado como `João Silva`.
- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-026 — Nome com espaços no início e no final

- **Requisito relacionado:** ESP-001.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o sistema remove os espaços extras do início e do
  final do Nome antes de realizar o cadastro.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `  João Silva  `;
  - E-mail: `joao.espacos@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `  João Silva  ` no campo Nome.
2. Informar o e-mail `joao.espacos@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve remover os espaços do início e do final do Nome.
- O nome deve ser registrado como `João Silva`.
- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-027 — E-mail com espaços no início e no final

- **Requisito relacionado:** ESP-001.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se o sistema remove os espaços extras do início e do
  final do E-mail antes de validar e realizar o cadastro.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `  joao@example.com  `;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João Silva` no campo Nome.
2. Informar `  joao@example.com  ` no campo E-mail.
3. Informar a senha `QA manual #1!`.
4. Selecionar o botão Cadastrar.

### Resultado esperado

- O sistema deve remover os espaços do início e do final do E-mail.
- O e-mail deve ser registrado como `joao@example.com`.
- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-028 — E-mail com espaço interno

- **Requisito relacionado:** EML-002.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema recusa um endereço de e-mail que contém
  espaço interno.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `joao @example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João Silva` no campo Nome.
2. Informar `joao @example.com` no campo E-mail.
3. Sair do campo E-mail.
4. Informar a senha `QA manual #1!`.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-029 — Todos os campos obrigatórios vazios

- **Requisitos relacionados:** NOM-006, EML-001, SEN-001, CAD-004, CAD-006,
  CAD-007, CAD-008 e CAD-009.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se o sistema apresenta simultaneamente os erros de
  todos os campos obrigatórios vazios.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Nome: vazio;
  - E-mail: vazio;
  - Senha: vazia.

### Passos

1. Selecionar o campo Nome e sair dele sem preenchê-lo.
2. Selecionar o campo E-mail e sair dele sem preenchê-lo.
3. Selecionar o campo Senha e sair dele sem preenchê-lo.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Nome é obrigatório” deve aparecer abaixo do campo Nome.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- A mensagem “Senha é obrigatória” deve aparecer abaixo do campo Senha.
- Os três campos devem ficar destacados em vermelho.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-030 — Clique duplo no botão Cadastrar

- **Requisitos relacionados:** CAD-005 e CAD-010.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se cliques rápidos e repetidos no botão Cadastrar não
  criam usuários duplicados.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `clique.duplo@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João Silva` no campo Nome.
2. Informar o e-mail `clique.duplo@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar duas vezes rapidamente o botão Cadastrar.

### Resultado esperado

- O botão deve ficar temporariamente desabilitado durante o processamento.
- Apenas um cadastro deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida uma única vez.

### Execução

- **Resultado obtido (simulado):** ao selecionar rapidamente o botão duas
  vezes, o sistema processou as duas solicitações e criou dois cadastros com o
  mesmo e-mail.
- **Status:** Reprovado.
- **Bug relacionado:** BUG-001.

## CT-031 — Limpeza dos campos após cadastro

- **Requisito relacionado:** CAD-011.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se os campos são limpos automaticamente após um
  cadastro realizado com sucesso.
- **Pré-condição:** usuário está na tela de cadastro e o e-mail de teste ainda
  não foi utilizado.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `limpeza.campos@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João Silva` no campo Nome.
2. Informar o e-mail `limpeza.campos@example.com`.
3. Informar a senha `QA manual #1!`.
4. Selecionar o botão Cadastrar.
5. Observar o conteúdo dos campos após a confirmação do cadastro.

### Resultado esperado

- O usuário deve ser criado.
- A mensagem “Cadastro realizado com sucesso” deve ser exibida.
- Os campos Nome, E-mail e Senha devem ficar vazios.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-032 — Manutenção dos campos válidos após erro

- **Requisito relacionado:** CAD-012.
- **Tipo de teste:** negativo.
- **Objetivo:** verificar se os dados válidos permanecem preenchidos quando
  apenas um campo apresenta erro.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `joao.example.com`, sem o caractere `@`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `João Silva` no campo Nome.
2. Informar `joao.example.com` no campo E-mail.
3. Sair do campo E-mail.
4. Informar a senha `QA manual #1!`.
5. Observar os campos e o botão após a apresentação do erro.

### Resultado esperado

- O usuário não deve ser criado.
- A mensagem “Informe um e-mail válido” deve aparecer abaixo do campo E-mail.
- O campo E-mail deve ficar destacado em vermelho.
- O Nome e a Senha devem permanecer preenchidos sem alterações.
- O botão Cadastrar deve permanecer desabilitado.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-033 — Remoção imediata do erro após correção

- **Requisito relacionado:** CAD-013.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar se a mensagem e o destaque de erro desaparecem
  imediatamente após a correção do campo.
- **Pré-condição:** usuário está na tela de cadastro.
- **Dados de teste:**
  - Nome inicial: `J`;
  - Nome corrigido: `João Silva`;
  - E-mail: `correcao.imediata@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Informar `J` no campo Nome.
2. Sair do campo Nome.
3. Confirmar a apresentação do erro no campo Nome.
4. Informar o e-mail `correcao.imediata@example.com`.
5. Informar a senha `QA manual #1!`.
6. Corrigir o Nome para `João Silva`.

### Resultado esperado

- Antes da correção, o campo Nome deve ficar destacado em vermelho e apresentar
  a mensagem “Nome deve conter entre 2 e 100 caracteres”.
- Após a correção, a mensagem e o destaque vermelho devem desaparecer
  imediatamente.
- Os outros campos devem permanecer preenchidos sem alterações.
- O botão Cadastrar deve ser habilitado.
- O cadastro não deve ocorrer automaticamente.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.

## CT-034 — Estado inicial e habilitação do botão

- **Requisitos relacionados:** EST-001, EST-002, EST-003, EST-004 e CAD-003.
- **Tipo de teste:** positivo.
- **Objetivo:** verificar os elementos iniciais da tela e a habilitação do botão
  Cadastrar somente após o preenchimento válido dos campos.
- **Pré-condição:** usuário ainda não preencheu a tela de cadastro e o e-mail de
  teste não foi utilizado.
- **Dados de teste:**
  - Nome: `João Silva`;
  - E-mail: `habilitar.botao@example.com`;
  - Senha: `QA manual #1!`.

### Passos

1. Abrir a tela de cadastro.
2. Confirmar a presença dos campos Nome, E-mail e Senha e do botão Cadastrar.
3. Observar o estado inicial do botão Cadastrar.
4. Informar `João Silva` no campo Nome.
5. Informar o e-mail `habilitar.botao@example.com`.
6. Informar a senha `QA manual #1!`.
7. Observar novamente o estado do botão Cadastrar.

### Resultado esperado

- Os três campos e o botão Cadastrar devem estar visíveis.
- O botão Cadastrar deve estar inicialmente desabilitado.
- Depois que todos os campos estiverem válidos, o botão deve ser habilitado.
- O cadastro não deve ocorrer automaticamente.

### Execução

- **Resultado obtido (simulado):** comportamento correspondente ao resultado
  esperado.
- **Status:** Aprovado.
