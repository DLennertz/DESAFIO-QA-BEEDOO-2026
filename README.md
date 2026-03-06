# DESAFIO-QA-BEEDOO-2026

## 1. Introdução

Este repositório apresenta a análise e os testes realizados na aplicação de cadastro e listagem de cursos disponibilizada no desafio técnico.

O objetivo foi explorar a aplicação, identificar seus fluxos principais, criar cenários de teste, executar os testes e registrar possíveis problemas encontrados.

---

# 2. Objetivo da aplicação

A aplicação tem como objetivo permitir o cadastro e a visualização de cursos.

O usuário pode inserir informações sobre um curso através de um formulário e visualizar os cursos cadastrados em uma lista.

Além disso, a aplicação permite excluir cursos cadastrados.

---

# 3. Estrutura do formulário

Durante a exploração da aplicação foi identificado que o formulário contém os seguintes campos:

• Nome do curso
• Descrição do curso
• Instrutor
• URL da imagem
• Data de início
• Data de fim
• Número de vagas
• Tipo de curso (Online ou Presencial)

Foi observado também um comportamento dinâmico no formulário:

• Quando o tipo de curso é **Online**, aparece o campo **Link de inscrição**
• Quando o tipo de curso é **Presencial**, aparece o campo **Endereço**

---

# 4. Fluxos identificados

Durante a análise da aplicação foram identificados os seguintes fluxos principais:

1. Cadastro de curso
   O usuário preenche os dados do curso e realiza o cadastro.

2. Listagem de cursos
   Os cursos cadastrados são exibidos em uma lista.

3. Exclusão de cursos
   O usuário pode remover cursos cadastrados através da opção de delete.

---

# 5. Pontos críticos para teste

Os pontos considerados mais críticos para teste foram:

• Validação de campos obrigatórios
• Validação de datas (data início e fim)
• Validação de campos numéricos
• Comportamento dinâmico do campo tipo de curso
• Persistência dos dados cadastrados
• Exclusão correta de cursos

---

# 6. Estratégia de testes

Durante a análise foram utilizados os seguintes tipos de teste:

• Testes exploratórios
• Testes funcionais
• Testes negativos
• Testes de validação de campos

Os cenários de teste foram elaborados considerando tanto o fluxo principal da aplicação quanto possíveis comportamentos inesperados.

---

# 7. Cenários e casos de teste

Os cenários e casos de teste foram documentados na planilha abaixo:

[LINK GOOGLE SHEETS]

---

# 8. Execução dos testes

Os cenários criados foram executados diretamente na aplicação.

Durante a execução foram registradas evidências em forma de prints para comprovar os resultados dos testes.

---

# 9. Evidências

As evidências da execução dos testes podem ser acessadas no link abaixo:

[LINK GOOGLE DRIVE]

---

# 10. Bugs encontrados

Os bugs identificados durante os testes foram documentados no relatório disponível neste repositório.
