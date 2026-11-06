# 👋 Boas-vindas

Olá e seja muito **bem-vindo(a)** ao nosso minicurso de **Introdução ao Desenvolvimento Back-End com Python: FastAPI**!

Se você já se perguntou **o que acontece por trás de um site ou aplicativo quando você clica em um botão, como os dados são guardados e como o front-end conversa com o servidor**, este curso foi pensado para responder exatamente essa pergunta. Sendo assim, ao longo desses **cinco dias**, aprenderemos desde os conceitos básicos da web e de APIs até a construção de uma **API completa**, com validação de dados, persistência em arquivo e tratamento de erros.

Você aprenderá a criar desde uma **única rota** até um **CRUD completo**, passando por **modelos de dados com Pydantic**, **organização de projeto em módulos** e **regras de negócio**. E mais do que apenas copiar código, o objetivo é entender **como uma API funciona por dentro e por que cada parte do código existe**.

---

# 🚀 Ao final do curso...

Você terá desenvolvido **sua própria API do zero**, tornando-se capaz de:

- **Aplicar** os conceitos de web, cliente-servidor e API REST na construção de um servidor real;
- **Familiarizar-se** com o ecossistema do FastAPI, do Pydantic e da documentação automática (Swagger);
- **Implementar** rotas com parâmetros, validação de dados e tratamento de erros;
- **Manejar** ferramentas essenciais do dia a dia de quem desenvolve (ambiente virtual, terminal, Git e GitHub);
- **Compreender** como organizar um projeto de forma limpa e profissional.

---

# 🎯 Objetivo do Curso

Neste minicurso, você construirá uma **base sólida em desenvolvimento back-end**, partindo dos conceitos de web e de uma primeira rota "Hello, Web!" até uma API completa, modular e testada.

Ao final do curso, você será capaz de:

- [x] **Compreender** o modelo cliente-servidor, o que é uma API REST, o formato JSON e os códigos de status HTTP;
- [x] **Criar** servidores e rotas com FastAPI, usando parâmetros de caminho (*path*) e de consulta (*query*);
- [x] **Modelar** e validar dados com Pydantic, protegendo a API contra entradas inválidas;
- [x] **Persistir** dados em arquivos JSON e organizar o código em módulos (`main.py`, `models.py` e `database.py`);
- [x] **Implementar** um CRUD completo com tratamento de erros (404 e 400) e regras de negócio.

---

# 📦 Pré-requisitos

Para acompanhar o conteúdo com tranquilidade, é esperado ter:

- **Conhecimentos básicos de lógica de programação**: variáveis, condicionais, laços, funções e estruturas de dados simples.

Esses conhecimentos fornecem a base necessária para absorver os tópicos de desenvolvimento web abordados durante o minicurso. Ao longo das aulas, faremos comparações com **C++** sempre que isso ajudar a entender algo novo em Python.

:::{important}
Alguns conceitos práticos específicos **serão aprofundados durante as aulas**. Sendo assim, ao longo do minicurso faremos introduções graduais a assuntos como:

- **Python para web**: dicionários, tipagem, decoradores e manipulação de arquivos;
- **Terminal e Git**: ambiente virtual, instalação de pacotes e compartilhamento de código no GitHub.

**Não se preocupe** caso precise de reforço nesses conteúdos: eles serão apresentados de forma intuitiva conforme forem necessários.
:::

---

# 🛠️ Como o curso será conduzido

O minicurso é estruturado em torno da **evolução prática**: da primeira rota ao projeto final, construindo a cada dia uma peça a mais da sua API.

Cada aula é dividida em **quatro blocos de cerca de uma hora**: os três primeiros apresentam o conteúdo com exemplos ao vivo, e o último é um **desafio prático**, no qual você aplica o que aprendeu de forma autônoma. Os participantes realizarão **atividades hands-on** a cada dia, testando as rotas diretamente no navegador por meio do Swagger e vendo instantaneamente o resultado de cada alteração no código.

:::{note}
Este minicurso é **fortemente baseado em prática**.

Cada novo conceito apresentado — seja uma rota, um modelo do Pydantic, a leitura de um arquivo JSON ou um tratamento de erro — será **implementado e testado na prática**, permitindo consolidar o aprendizado imediatamente.
:::

---

# 📅 Cronograma

## 🟢 Dia 1 — Fundamentos da Web e Primeiro Servidor

- **Introdução à Web e APIs**: Modelo cliente-servidor, API REST, formato JSON e códigos de status HTTP (200, 400, 404 e 500)
- **Preparação do Ambiente**: Ambiente virtual (*venv*) e instalação do FastAPI e do Uvicorn
- **Hello, Web!**: Criação do `main.py`, decoradores de função e a primeira rota com `@app.get("/")`
- **Rodando a Aplicação**: Execução do servidor e recarregamento automático durante o desenvolvimento
- **Swagger**: Tour pela documentação automática gerada no endpoint `/docs`
- **Parâmetros de Rota**: *Path parameters*, *query parameters* e conversão automática de tipos
- **Prática**: Desafio da Calculadora API, com rotas aritméticas, operações combinadas e proteção contra divisão por zero

---

## 🔵 Dia 2 — Pydantic e Rotas POST/GET

- **Dicionários e JSON**: Revisão de dicionários em Python e a ponte entre o JSON da web e o dicionário do Python
- **Modelos de Dados**: Dados na URL vs. corpo da requisição e criação de modelos com `BaseModel`
- **Rotas POST e GET**: Cadastro e listagem de itens em uma lista em memória, com `status_code=201`
- **Busca por ID**: Rota `GET` com parâmetro de caminho percorrendo a lista
- **Validações Avançadas**: `Field`, `EmailStr`, tipos aninhados e o erro 422
- **Filtros**: *Query parameters* aplicados sobre a lista de dados
- **Prática**: Desafio do Sistema de Cadastro Criterioso, com validação de usuários (nome, e-mail e senha)

---

## 🟡 Dia 3 — Persistência em JSON e Organização do Projeto

- **Por que os dados somem?**: Memória volátil vs. disco
- **Leitura e Escrita de Arquivos**: Função `open()`, modos de abertura e *context managers* (`with open`)
- **O módulo `json`**: `json.dump()`, `json.load()` e os parâmetros `indent` e `ensure_ascii`
- **Conectando a API ao JSON**: Fluxo ler > modificar > salvar, `.model_dump()` e geração automática de ID
- **Refatoração e Módulos**: Imports, responsabilidade única e divisão do projeto em `main.py`, `models.py` e `database.py`
- **Prática**: Desafio da Lista de Afazeres Persistente, com tarefas salvas em `tarefas.json`

---

## 🟠 Dia 4 — Tratamento de Erros, Regras de Negócio e CRUD Completo

- **Tratamento de Erros**: `HTTPException`, erros do cliente (4xx) vs. erros do servidor (5xx) e o status 404
- **Regras de Negócio**: Diferença entre erro de formato (422) e regra violada (400)
- **Rota DELETE**: Remoção de itens com persistência no arquivo JSON
- **Filtros no GET**: Parâmetros de consulta opcionais para filtrar resultados
- **Rota PUT**: Atualização de recursos existentes e fechamento do ciclo CRUD
- **Prática**: Desafio do Sistema Bancário Simples, com transferências entre contas, verificação de saldo e persistência dos valores

---

## 🔴 Dia 5 — Hackathon e Projeto Final

- **Planejamento**: Escolha do tema (livre ou entre Inventário de RPG, Gerenciador de Tarefas e Cadastro de Alunos), definição das rotas e dos atributos do Pydantic
- **Desenvolvimento Autônomo**: Construção da API com CRUD completo, leitura e escrita em JSON, separação em módulos e tratamento de erros (404 e 400)
- **Code Review e Testes**: Compartilhamento do repositório no GitHub e teste da API de outro grupo pelo Swagger
- **Prática**: Hackathon em grupo, com o professor atuando como *Tech Lead*, tirando dúvidas e destravando problemas

---

# 💻 Ferramentas utilizadas

Durante o curso utilizaremos principalmente:

- **Python**
- **FastAPI** e **Uvicorn**
- **Pydantic**
- **Swagger** (documentação automática em `/docs`)
- **VS Code** e **terminal**
- **Git** e **GitHub**

Todo o material e código base serão disponibilizados pelos organizadores.

---

# 🤝 Suporte

Durante todo o minicurso, os organizadores estarão disponíveis para **esclarecer dúvidas** e **auxiliar na implementação** das atividades propostas.

**Não tenha receio de perguntar!**

Desenvolvimento back-end envolve bastante **lógica**, **programação** e **experimentação**, e é completamente normal precisar de ajuda durante o processo.

---

Esperamos que este minicurso desperte sua curiosidade pela área e mostre que, por trás de **cada site e aplicativo**, existe uma enorme quantidade de **lógica**, **organização** e **engenharia**.

# **Vamos começar! 🚀**