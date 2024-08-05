# TCC-Salao

## Projeto Final de ADS - Faculdade Impacta de Tecnologia 2022

### Índice
1. [Descrição do Projeto](#descrição-do-projeto)
2. [Funcionalidades](#funcionalidades)
3. [Tecnologias Utilizadas](#tecnologias-utilizadas)
4. [Instalação e Execução](#instalação-e-execução)
    - [Pré-requisitos](#pré-requisitos)
    - [Como executar o projeto](#como-executar-o-projeto)
5. [Estrutura do Projeto](#estrutura-do-projeto)
    - [Models Folder](#models-folder)
    - [Static Folder](#static-folder)
    - [Templates Folder](#templates-folder)

### Descrição do Projeto
Este projeto é o trabalho de conclusão de curso para o curso de Análise e Desenvolvimento de Sistemas da Faculdade Impacta de Tecnologia. O projeto consiste em um sistema de gerenciamento de salão de beleza, que permite agendar serviços, gerenciar clientes, funcionários e usuários do sistema.

### Funcionalidades
- Adicionar, consultar, alterar e deletar usuários, clientes e funcionários.
- Agendar serviços com data e hora.
- Interface amigável para navegação e utilização do sistema.

### Tecnologias Utilizadas
- Flask
- SQLAlchemy
- HTML/CSS
- jQuery
- Bootstrap

### Instalação e Execução

#### Pré-requisitos
- Python 3.x
- Flask
- SQLAlchemy
- jQuery

#### Como executar o projeto
1. Clone o repositório:
    ```bash
    git clone [https://github.com/seu-usuario/tcc-salao.git](https://github.com/noudas/TCC-Salao.git)
    ```
2. Navegue até a pasta do projeto:
    ```bash
    cd tcc-salao
    ```
3. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```
4. Configure o banco de dados no arquivo `app_server.py`.
5. Execute a aplicação:
    ```bash
    flask run
    ```

### Estrutura do Projeto

#### Models Folder:
1. **agenda_models.py**
    - `def adicionar_agendamento(username, email, telefone, data, servico)`
        - Função para adicionar um novo agendamento no sistema.
        - Utiliza os parâmetros: `username`, `email`, `telefone`, `data`, `servico`.
        - Adiciona o agendamento na base de dados e confirma a transação.

2. **cliente_models.py**
    - `def adicionar_user(username, password, email, telefone)`
        - Adiciona um novo cliente no sistema.
    - `def consultar_user(email)`
        - Consulta dados de um cliente pelo email.
    - `def alterar_user(username, password, email, telefone)`
        - Altera os dados de um cliente pelo email.
    - `def deleta_user(email)`
        - Deleta um cliente pelo email.

3. **funcionario_models.py**
    - Mesmas funções e estrutura do `cliente_models.py`, porém para gerenciar funcionários.

4. **user_models.py**
    - Mesmas funções e estrutura do `cliente_models.py`, porém para gerenciar usuários do sistema.

#### Static Folder:
- **bootstrap.css**
- **profile.css**
- **styles.css**
- **styles_form.css**

#### Templates Folder:
1. **agendar_servico.html**
    - Formulário para agendar serviços.
    - Inclui integração com jQuery UI para seleção de data e hora.

2. **consulta_user.html**
    - Página para consulta de dados de usuários via email.
    - Mostra os dados do usuário caso encontrado.

3. **dashboard.html**
    - Página principal do sistema.
    - Contém links para as principais funcionalidades como perfil, agendamento de serviços e consulta de usuários.

4. **home.html**
    - Página inicial com links para login e registro.

5. **login.html**
    - Página de login.
    - Inclui formulário de login estilizado com `styles_form.css`.

6. **profile.html**
    - Página de perfil do usuário.
    - Mostra informações do usuário atual e permite editar os dados de perfil.
