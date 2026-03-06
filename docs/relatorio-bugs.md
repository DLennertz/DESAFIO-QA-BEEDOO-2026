BUG 01 — Sistema permite cadastro com campos obrigatórios vazios

Severidade: Alta
Impacto: Permite cadastro de cursos com informações incompletas.

Casos de teste relacionados

CT02, CT03, CT04, CT05, CT06, CT07

Passos para reproduzir

1. Acessar o formulário de cadastro de cursos

2. Deixar um dos campos obrigatórios vazio (ex.: nome do curso, descrição, instrutor, datas ou número de vagas)

3. Preencher os demais campos

4. Clicar em Cadastrar

Resultado atual

O sistema permite realizar o cadastro do curso e exibe a mensagem de sucesso.

Resultado esperado

## O sistema deveria impedir o cadastro e exibir uma mensagem informando que os campos obrigatórios devem ser preenchidos.

BUG 02 — Sistema aceita valores inválidos no campo número de vagas

Severidade: Média
Impacto: Permite inserção de valores inconsistentes no cadastro.

Casos de teste relacionados

CT08, CT09

Passos para reproduzir

1. Acessar o formulário de cadastro

2. Inserir valor inválido no campo Número de vagas (ex.: número negativo ou zero)

3. Preencher os demais campos

4. Clicar em Cadastrar

Resultado atual

O sistema permite realizar o cadastro e exibe mensagem de sucesso.

Resultado esperado

## O sistema deveria validar o campo e impedir valores inválidos.

BUG 03 — Sistema permite cadastro com datas inconsistentes

Severidade: Média
Impacto: Cursos podem ser cadastrados com datas inválidas.

Casos de teste relacionados

CT11, CT13, CT14

Passos para reproduzir

1. Acessar o formulário de cadastro

2. Inserir data de início maior que a data de fim ou datas inválidas

3. Preencher os demais campos

4. Clicar em Cadastrar

Resultado atual

O sistema permite cadastrar o curso e exibe mensagem de sucesso.

Resultado esperado

## O sistema deveria validar as datas e impedir o cadastro quando as datas forem inconsistentes.

BUG 04 — Sistema permite cadastro de curso Online sem link de inscrição

Severidade: Média
Impacto: Cursos online podem ser cadastrados sem informação essencial.

Caso de teste relacionado

CT19

Passos para reproduzir

1. Acessar o formulário de cadastro

2. Selecionar tipo de curso Online

3. Não preencher o campo Link de inscrição

4. Preencher os demais campos

5. Clicar em Cadastrar

Resultado atual

O sistema permite cadastrar o curso e exibe mensagem de sucesso.

Resultado esperado

## O sistema deveria exigir o preenchimento do campo Link de inscrição para cursos online.

BUG 05 — Sistema permite cadastro de curso presencial sem endereço

Severidade: Média
Impacto: Cursos presenciais podem ser cadastrados sem local definido.

Caso de teste relacionado

CT20

1. Passos para reproduzir

2. Acessar o formulário de cadastro

3. Selecionar tipo de curso Presencial

4. Não preencher o campo Endereço

5. Preencher os demais campos

6. Clicar em Cadastrar

Resultado atual

O sistema permite cadastrar o curso e exibe mensagem de sucesso.

Resultado esperado

## O sistema deveria exigir o preenchimento do campo Endereço para cursos presenciais.

BUG 06 — Sistema aceita URL inválida no campo imagem

Severidade: Baixa
Impacto: Pode permitir dados incorretos no sistema.

Caso de teste relacionado

CT22

Passos para reproduzir

1. Acessar o formulário de cadastro

2. Inserir texto inválido no campo URL da imagem

3. Preencher os demais campos

4. Clicar em Cadastrar

Resultado atual

O sistema permite cadastrar o curso e exibe mensagem de sucesso.

Resultado esperado

## O sistema deveria validar o formato da URL antes de permitir o cadastro.

BUG 07 — Curso não é excluído da listagem (API retorna 405)

Severidade: Alta
Impacto: Funcionalidade de exclusão não funciona.

Casos de teste relacionados

CT27, CT28

Passos para reproduzir

1. Cadastrar um curso

2. Localizar o curso na listagem

3. Clicar no botão Delete

4. Confirmar exclusão no alerta exibido

Resultado atual

Após confirmar a exclusão, o curso continua sendo exibido na listagem.

Durante a análise no DevTools → Network, foi identificado que a requisição enviada para a API retorna o status:

405 Method Not Allowed

Isso indica que o método HTTP utilizado na requisição não é permitido pelo endpoint da API.

Resultado esperado

O sistema deveria enviar uma requisição válida para a API e remover o curso da listagem após a confirmação da exclusão.
