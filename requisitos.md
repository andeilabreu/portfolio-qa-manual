# Requisitos — Cadastro de usuário

## Situação

Primeira versão definida e confirmada por Andeil. Os requisitos receberam
identificadores para permitir a ligação com os futuros casos de teste.

## Requisitos confirmados

### Estrutura da tela

- **EST-001:** a tela possui o campo Nome.
- **EST-002:** a tela possui o campo E-mail.
- **EST-003:** a tela possui o campo Senha.
- **EST-004:** a tela possui o botão Cadastrar.

## Regras de funcionamento

### Tratamento de espaços

- **ESP-001:** o sistema deverá remover espaços extras do início e do final do
  nome e do e-mail.
- **ESP-002:** os espaços digitados na senha não deverão ser removidos nem
  alterados.

### Nome

- **NOM-001:** o preenchimento será obrigatório.
- **NOM-002:** o tamanho mínimo será de 2 caracteres.
- **NOM-003:** o tamanho máximo será de 100 caracteres.
- **NOM-004:** serão aceitas letras com ou sem acentos, espaços, hífen e
  apóstrofo.
- **NOM-005:** números não serão aceitos. Se o nome contiver números, o sistema
  deverá exibir a mensagem “Nome contém caracteres não permitidos. Use letras,
  espaços, hífen ou apóstrofo”, destacar o campo e não criar o usuário.
- **NOM-006:** se o campo estiver vazio, o sistema deverá exibir a mensagem
  “Nome é obrigatório”, destacar o campo e não criar o usuário.
- **NOM-007:** se o nome possuir menos de 2 ou mais de 100 caracteres, o sistema
  deverá exibir a mensagem “Nome deve conter entre 2 e 100 caracteres”,
  destacar o campo e não criar o usuário.

### E-mail

- **EML-001:** o preenchimento será obrigatório. Se o campo estiver vazio, o
  sistema deverá exibir a mensagem “Informe um e-mail válido”, destacar o campo
  e não criar o usuário.
- **EML-002:** o endereço deverá possuir formato válido, como
  `nome@dominio.com`. Se o formato for inválido, o sistema deverá exibir a
  mensagem “Informe um e-mail válido”, destacar o campo e não criar o usuário.
- **EML-003:** cada e-mail poderá pertencer a apenas um cadastro.
- **EML-004:** a verificação de duplicidade deverá ignorar diferenças entre
  letras maiúsculas e minúsculas.
- **EML-005:** se o e-mail já estiver registrado, o sistema deverá informar o
  problema com a mensagem “E-mail já cadastrado”, destacar o campo e não deverá
  criar outro usuário.

### Senha

- **SEN-001:** o preenchimento será obrigatório. Se o campo estiver vazio, o
  sistema deverá exibir a mensagem “Senha é obrigatória”, destacar o campo e
  não criar o usuário.
- **SEN-002:** o tamanho mínimo será de 12 caracteres. Se a senha possuir menos
  de 12 caracteres, o sistema deverá exibir a mensagem “A senha deve conter no
  mínimo 12 caracteres”, destacar o campo e não criar o usuário.
- **SEN-003:** o tamanho máximo será de 64 caracteres. Se a senha possuir mais
  de 64 caracteres, o sistema deverá exibir a mensagem “A senha deve conter no
  máximo 64 caracteres”, destacar o campo e não criar o usuário.
- **SEN-004:** serão aceitas letras, números, espaços e símbolos, incluindo
  hífen.
- **SEN-005:** nenhuma combinação específica de tipos de caracteres será
  obrigatória.
- **SEN-006:** o sistema deverá manter exatamente os caracteres digitados, sem
  substituir espaços por hífens.
- **SEN-007:** os caracteres da senha deverão permanecer ocultos durante a
  digitação.

### Botão Cadastrar

- **CAD-001:** quando todos os dados forem válidos, o sistema deverá criar o
  usuário e exibir a mensagem “Cadastro realizado com sucesso”.
- **CAD-002:** o sistema não deverá criar um segundo usuário com o mesmo
  e-mail.
- **CAD-003:** o botão deverá permanecer disponível mesmo quando existirem
  campos inválidos.
- **CAD-004:** ao selecionar o botão, o sistema deverá validar todos os campos.
- **CAD-005:** após o primeiro clique, o botão deverá ficar temporariamente
  desabilitado enquanto o cadastro estiver sendo processado.
- **CAD-006:** uma mensagem clara deverá ser exibida abaixo de cada campo
  inválido.
- **CAD-007:** o primeiro campo com erro deverá ser destacado.
- **CAD-008:** o usuário não deverá ser criado enquanto existir algum erro de
  validação.

## Observação sobre o exercício anterior

A regra de senha com exatamente cinco dígitos foi usada somente para aprender
valores-limite. Ela não será adotada neste projeto profissional porque oferece
segurança insuficiente.
