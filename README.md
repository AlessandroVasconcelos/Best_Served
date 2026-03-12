# Best Servd - Sistema de Agendamento de Reservas de Mesas em Restaurantes

**Best Servd** é uma aplicação web que conecta restaurantes e clientes, permitindo o agendamento de mesas de forma prática e eficiente. O sistema possui três tipos de usuários com permissões específicas:  
- **Cliente**: cadastra-se, busca restaurantes, faz reservas, além de avaliar estabelecimentos.  
- **Restaurante**: cadastra seu estabelecimento, gerencia mesas, cardápio, horários e confirma ou cancela reservas.  
- **Administrador**: gerencia toda a plataforma, aprova os cadastros dos restaurantes, visualiza os usuários cadastrados no sistema e garante a segurança geral da aplicação.

## 📋 Funcionalidades Principais

- **Gerenciar disponibilidade de mesas**
- **Cadastrar cliente**  
- **Cadastrar restaurante**
- **Atualizar/Excluir perfil**  
- **Reservar mesa**
- **Cancelar reserva**  
- **Buscar restaurantes**   
- **Avaliar restaurante**   
- **Visualizar disponibilidade de mesas**  
- **Visualizar cardápio do restaurante**
  
## **🚀 Como Rodar o Projeto**

Este guia descreve os passos necessários para configurar e executar o projeto localmente. O projeto é dividido em **backend (api)** e **frontend**, que devem ser executados em terminais separados.

### 1. Configuração do Backend (API)

O backend gerencia a lógica da aplicação e a conexão com o banco de dados.

1.  **Abra um terminal** e navegue até o diretório da API:
    ```bash
    cd "C:\caminho\para\seu\projeto\Best_Served-main\api"
    ```

2.  **Crie o arquivo de ambiente**:
    Na pasta `api`, crie um arquivo chamado `.env`. Este arquivo armazena as chaves e configurações sensíveis. Uma vez criada a sua conta no MongoDB cole a URL do seu database no arquivo env, depois gere um hash aleatório que servirá como chave de autenticação JWT. Defina a porta em que o seu sistema irá rodar, por padrão escolha a porta 3000.

    ```env
    # URL de conexão com o banco de dados MongoDB
    DATABASE_URL="mongodb+srv://seu_usuario_mongodb:P3bJaUTgun0qmQnL@users.ybsabac.mongodb.net/Users?retryWrites=true&w=majority&appName=Users"

    # Chave secreta para autenticação JWT
    JWT_SECRET="8027*******************************************************55f7"
    
    # Porta em que o servidor irá rodar
    PORT=3000
    ```

3.  **Gere o cliente do Prisma**:
    Este comando lê seu schema do banco de dados e gera o código necessário para a aplicação interagir com ele.
    ```bash
    npx prisma generate
    ```

4.  **Inicie o servidor do backend**:
    O comando abaixo inicia o servidor e o reinicia automaticamente a cada alteração nos arquivos (`--watch`).
    ```bash
    node --watch server.js
    ```
    Após executar, mantenha este terminal aberto.

---

### 2. Configuração do Frontend

O frontend é a interface visual da aplicação. **Abra um novo terminal** para executar estes passos.

1.  Navegue até o diretório do `frontend`:
    ```bash
    cd "C:\caminho\para\seu\projeto\Best_Served-main\frontend"
    ```

2.  **Instale as dependências**:
    Este comando baixa todas as bibliotecas necessárias para o frontend.
    ```bash
    npm install
    ```

3.  **Inicie o servidor de desenvolvimento**:
    ```bash
    npm run dev
    ```
    Acesse a URL fornecida no terminal no seu navegador para ver a aplicação.

---

### 3. Visualizar o Banco de Dados (Opcional) 

O Prisma Studio fornece uma interface gráfica para visualizar e editar os dados em tempo real.

1.  **Abra um terceiro terminal** e navegue novamente até o diretório da `api`:
    ```bash
    cd "C:\caminho\para\seu\projeto\Best_Served-main\api"
    ```

2.  **Inicie o Prisma Studio**:
    ```bash
    npx prisma studio
    ```
    Isso abrirá uma nova aba no seu navegador, permitindo que você gerencie o banco de dados facilmente.

## **🛠️ Tecnologias Utilizadas**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![bcrypt](https://img.shields.io/badge/bcrypt-3383FF?style=for-the-badge&logo=keycdn&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
