
# Relacionamento one-to-one Laravel

Este é um tipo de relacionamento entre tabelas mais simples que existe. Mas que servirá como base de conhecimento para o entedimento dos outros tipos de relacionamentos mais complexos.

Neste exemplo vamos relacionar uma tabela de `usuários` com uma tabela `endereços`. Onde um usuário pode conter apenas um endereço, e um endereço pertence apenas a um usuário.

Desta forma, evitamos que a tabela `usuários` contenha vários campos.


## Instalação

Ao instalar o laravel, o mesmo já possui a migration responsável para criação da tabela `usuários`, então vamos criar apenas a migration responsável pela tabela de `endereços`.

### Instalação Laravel

é necessário ter o composer instalado.

```bash
composer create-project laravel/laravel example-app
```

## Criação da migration Address

Esse comando irá criar a model e a respectiva migration, tudo de uma vez.

```bash
php artisan make:model Address -m
```



## Arquivo migration address

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/migration_address.png?token=GHSAT0AAAAAAB7THWOYWTLOGC2YTAGEP6DIZAEWHAA)

### Execute o seguinte comando no seu terminal

```bash
php artisan migrate
```


Verifique agora que foi criada a tabela addresses, relacionada com a tabela users.
## Model Address

Na nossa Model Address vamos preencher a propriedade `fillable` do Model.

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/model_address.png?token=GHSAT0AAAAAAB7THWOZ5VEPOYCGSHK5GOB4ZAEWGHQ)
## Model User

Na nossa model User vamos criar a seguinte função que será responsável por declarar um relacionamento One to One.

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/function_endereco.png?token=GHSAT0AAAAAAB7THWOY252M4TKN3QKGNQYWZAEWNVA)
## Resultado do relacionamento

O Resultado do relacionamento deverá ficar como o da figura abaixo:

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/eer_diagrama_one_to_one.png?token=GHSAT0AAAAAAB7THWOZD2QLX7BOZWFNTUBIZAEXJNA)


## Testando com Tinker

Vamos testar nosso relacionamento criado usando o console interativo `Tinker`.

Para isso rode o seguinte comando no terminal dentro do seu projeto.

```bash
php artisan tinker
```
## Criando o primeiro usuário com o Tinker

Agora que estamos dentro do console interativo do laravel, vamos criar nosso primeiro usuário.

A escrita é e mesma como se estivéssemos dentro do nosso editor de código preferido, a diferença é que não precisamos verificar a resposta no nosso navegador. Tudo será feito no console do `Tinker`.

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/criando_usuario.png?token=GHSAT0AAAAAAB7THWOZ53BKOPQ4WCH2U6GQZAEWYYA)


## Criando Endereço e relacionando com usuário

Agora que criamos o primeiro usuário com `id=1`, vamos criar um endereço e relacionar com o usuário deste id.

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/criacao_address.png?token=GHSAT0AAAAAAB7THWOZNURWZIJ2X444JYP6ZAEXAYQ)


## Testando a relação One to One

Agora vamos realizar uma consulta no banco e testaremos a relação `on to one` criada.

Para isso, execute o seguinte comando no console do `Tinker`

```bash
App\Models\User::with('endereco')->findOrFail(1);
```

O resultado será o mostrado abaixo:

![App Screenshot](https://raw.githubusercontent.com/cleyton21/images/master/consulta_relacao_one_to_one.png?token=GHSAT0AAAAAAB7THWOZNRGVUG6TYMG4VGISZAEXGPQ)

Agora todos os dados são trazidos em conjunto com a relação criada.

Espero que tenha ajudado e aguardo sugestões de melhorias.


## Referência

 - [Relacionamentos Laravel](https://laravel.com/docs/10.x/eloquent-relationships#many-to-many-defining-the-inverse-of-the-relationship)



## 🚀 Sobre mim

### Olá, eu sou o Cleyton Fernando! 👋

- 🔭 Atualmente trabalho com Backend, sou dev, autodidata, apaixonado por software livre e amante de novas tecnologias. Atualmente estudando PHP, Laravel, vue.js.
- 🌱 Trabalho há 10 anos com tecnologia, desenvolvendo soluções para as mais diversas situações.
- 😄 Em busca de conhecimento e novos desafios.

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/cleyton-fernando-08b64812b/)


## 🛠 Habilidades
PHP, Laravel, Rest, Mysql, Javascript, HTML, CSS, Ajax, Linux, Docker, Docker Swarm...


## Suporte

Para suporte, mande um email para cfernando_21@hotmail.com.


## Criação da migration Address

Esse comando irá criar a model e a respectiva migration, tudo de uma vez.

```bash
php artisan make:model Address -m
```



## Autores

- [@cleyton21](https://github.com/cleyton21)

