# Ranking de Tempo Assistido

## Requisitos:
-  Git
-  Composer
-  PHP
-  MySQL

## Subir a API
Para testar o projeto, siga os passos descritos abaixo:

### Passo a passo
Clone Repositório
```sh
git clone https://github.com/Matheus-O-Silva/ranking-app.git
```

```sh
cd ranking-app
```

### Configuração

- Crie o arquivo `.env` (Veja .env.example)
- Configure um valor para `APP_KEY` com o comando:
```sh
 $ php artisan key:generate
 ```
- Configure um valor para `DB_PASSWORD` (Senha do root para o MySQL)
- Rode o comando:
```sh
 `composer install`
```
- Rode o comando abaixo para criar a estrutura do banco
```sh
 `php artisan migrate`
```
- Rode os comandos abaixo para popular as tabelas do banco:
```sh
php artisan db:seed --class=UserSeeder
php artisan db:seed --class=ChannelSeeder
php artisan db:seed --class=WatchedTimeSeeder
```
### Rodando a aplicação
```sh
$ php artisan serve # http://localhost:8000
```

### Acesse o Ranking Agrupado por canais pelo endpoint:
[http://localhost:8000/channels-ranking](http://localhost:8000/channels-ranking)

### Acesse o Ranking ordenado por Usuários pelo endpoint:
[http://localhost:8000/users-ranking](http://localhost:8000/users-ranking)

### A posição no Ranking de cada usuário está no campo 'place' dos objetos retornados
