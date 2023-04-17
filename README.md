# ilumeo_docker
Passos para executação do projeto.

# Rodando o docker
## Copia submodules do github 
`git submodule update --remote`

## Variaveís de ambiente
### Backend
Já está configurado no docker-compose, mas pode configurar o uso do .env também caso deseje <br />
PSQL_HOST=localhost                //Host postgress <br />
POSTGRES_PASSWORD=123456           //Senha postgres<br />
POSTGRES_USER=postgres             //User postgres<br />
POSTGRES_DB=ilumeo                 //Nome banco postgres<br />
PORT=3333                          //Porta do server node <br />
NODE_ENV=development               //Ambiente<br />
SECRET=eqewjqopejwqpoejqwepoqwjepo //Secret para gerar JWT<br />

### Frontend
Já está configurado para url ser na porta 3000 caso não tenha, mas pode descomentar a linha do `env_file em client` e criar o arquivo .env na raiz do projeto frontend 
com o `VITE_BASE_URL=http://localhost:3000`

## Docker Compose 
O docker compose cria um banco postgres, um server node js e a aplicação client em React.JS
`docker-compose up --build -d`

## Usuários registrados na SEED (Precisa rodar a seed no backend) (Códigos)
QUOkXwK,GM7K0QO,4SXXFMf

## Criar usuário
Pode utilizar a rota post do backend em `/users`, passando apenas o nome e ser gerado um novo código de usuário.

