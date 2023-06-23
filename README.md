## DESAFIO_PROJETO_MVC_SOFTMAKERS

## Nome: Diogo Felipe
## Email: diogoinformatica1@gmail.com
## Contato: (81)97103-9950

O projeto Seu-Pet é uma aplicação web desenvolvida em React que segue a estrutura do padrão de arquitetura Modelo-Visão-Controlador (MVC). Ele permite gerenciar uma lista de animais de estimação, fornecendo funcionalidades para adicionar, visualizar, editar e excluir animais da lista.

## Funcionalidades
Adicionar um novo animal de estimação, fornecendo nome, espécie e idade.
Visualizar a lista completa de animais de estimação cadastrados.
Editar as informações de um animal de estimação existente.
Excluir um animal de estimação da lista.
Como rodar o projeto em outro computador
Para executar o projeto em seu computador local, siga as etapas abaixo:

## Pré-requisitos
Node.js instalado (versão 12 ou superior)
Gerenciador de pacotes npm ou yarn
Passos
Faça o clone deste repositório para o seu ambiente local ou faça o download do código-fonte.

Abra o terminal ou prompt de comando e navegue até o diretório raiz do projeto.

Instale as dependências do projeto executando o seguinte comando:

## npm install
## npm install axios body-parser cors express moment mysql nodemon pg

ou

## yarn install

Com as dependências instaladas, você pode iniciar o servidor de desenvolvimento com o comando:
## npm start
ou

## yarn start
Aguarde até que o servidor de desenvolvimento seja iniciado. Após a compilação, você poderá acessar o projeto em seu navegador através do endereço:

http://localhost:3000
Agora você pode explorar todas as funcionalidades do projeto Seu-Pet em seu próprio computador.

## Tecnologias utilizadas:

## backend:

"dependencies": {
    "axios": "^1.4.0",
    "body-parser": "^1.20.2",
    "cors": "^2.8.5",
    "express": "^4.18.2",
    "moment": "^2.29.4",
    "mysql": "^2.18.1",
    "nodemon": "^2.0.20",
    "pg": "^8.11.0"
  },

  ## frontend:
  
    "dependencies": {
    "@testing-library/jest-dom": "^5.16.5",
    "@testing-library/react": "^13.4.0",
    "@testing-library/user-event": "^13.5.0",
    "axios": "^0.27.2",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-icons": "^4.9.0",
    "react-script": "^2.0.5",
    "react-scripts": "^5.0.1",
    "react-toastify": "^9.1.3",
    "styled-components": "^5.3.11",
    "web-vitals": "^2.1.4"
  },

  ## Banco de dados criado no PostgresSQL
  
  ## Crie o banco chamado seu-pet.
  ## Em seguida execute a seguite query para criar a tabela "Pets":
  
  CREATE TABLE IF NOT EXISTS public."Pets"
(
    id integer NOT NULL DEFAULT nextval('"Pets_id_seq"'::regclass),
    nome character varying(100) COLLATE pg_catalog."default" NOT NULL,
    idade integer NOT NULL,
    especie "enum_Pets_especie" NOT NULL,
    raca character varying(255) COLLATE pg_catalog."default" NOT NULL,
    "nomeDono" character varying(255) COLLATE pg_catalog."default" NOT NULL,
    "telefoneDono" character varying(255) COLLATE pg_catalog."default" NOT NULL,
    "createdAt" timestamp with time zone NOT NULL,
    "updatedAt" timestamp with time zone NOT NULL,
    CONSTRAINT "Pets_pkey" PRIMARY KEY (id)
)

TABLESPACE pg_default;

ALTER TABLE IF EXISTS public."Pets"
    OWNER to postgres;

GRANT ALL ON TABLE public."Pets" TO postgres;
  

React: biblioteca JavaScript para a construção da interface do usuário.
styled-components: biblioteca para estilização dos componentes utilizando CSS-in-JS.
axios: cliente HTTP para realizar requisições à API REST local.
react-toastify: biblioteca para exibição de notificações na interface.

## Estrutura MVC
O projeto Seu-Pet segue a arquitetura Modelo-Visão-Controlador (MVC). Essa estrutura separa as responsabilidades em três componentes principais:
Modelo (Model): Responsável pelo gerenciamento dos dados e regras de negócio.
Visão (View): Responsável pela interface do usuário, exibindo os dados e interagindo com o usuário.
Controlador (Controller): Responsável por receber as ações do usuário na interface e coordenar a interação entre a Visão e o Modelo.
Essa estrutura permite uma melhor organização e separação de responsabilidades no projeto, facilitando a manutenção e o desenvolvimento de novas funcionalidades.
