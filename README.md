# Next Level Week 02

Projeto Proffys - Cadastro de professores e aulas - Next Level Week 2 - Rocketseat

## Estrutura do Projeto

| Pasta | Descrição |
| ----------- | ----------- |
| ./server | API REST feita em Express e TypeScript e banco de dados SQLite |
| ./web | Interface web em RectJS e TypeScript |
| ./mobile | Interface mobile em ReactNative e TypeScript |


## Entidades

| Entidades | Atributos |
| ----------- | ----------- |
| users | id, name, avatar, whatsapp, bio |
| classes | id, subject, cost, user_id |
| class_schedule | id, week_day, from, to, class_id |
| connections | id, user_id, created_at |

## Funcionalidades

* Cadastrar aula
  * Cadastro de usuário
  * Cadastro de matéria
  * Cadastro de cronograma (dias e horários de aula)
* Listagem de aula, professor e cronograma
* Criar conexão
* Obter total de conexões

## Iniciando o projeto

Após clonar o projeto, é necessário atualizar as dependências e efetuar as migrações do banco de dados.

Baixar, migrar banco e executar Server (a partir da raiz; precisa ser executado primeiro)

```bash
cd server
yarn
yarn knex:migrate
```

Baixar e executar Web (a partir da raiz)
```bash
cd web
yarn
```

Baixar e executar Mobile (a partir da raiz)
```bash
cd mobile
yarn
```

## Configurações

Arquivo **./mobile/src/services/api.ts**

```javascript
// Substituir <server_ip_address> pelo endereço IP em que está executando o server
const api = axios.create({
	baseURL: 'http://<server_ip_address>:3333'
})
```