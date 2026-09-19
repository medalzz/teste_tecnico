
# Teste Técnico

Teste técnico para laravel junior

Feito com Docker, Laravel e Blade

## Requisitos

- [git](https://git-scm.com/downloads)
- [Docker](https://www.docker.com/)

## Endpoints

#### Home

```
  GET /
```

Página inicial. 
Contém um form que ativa a busca de entregas por cpf.
Um submit com o campo vazio busca todas as entregas


#### Lista de Entregas

```
  GET /entregas
```

| Parâmetro | Tipo     | Descrição                |
| :-------- | :------- | :------------------------- |
| `cpf`     | `string` |  Busca entrega por cpf     |


Página que mostra a lista de entregas baseado no cpf informado.
Clicar em uma das entregas abre um novo endpoint que mostra mais dados da mesma.


#### Dados da Entrega

```
  GET /entrega/${id}
```

|  Parâmetro  | Tipo |  Descrição                               |
|  :--------  | :--- | :--------------------------------------- |
|    `id`     |`int` | **Required**. Mostra os dados da entrega |

Mostra todos os dados relacionados a entrega com o ID informado, 
incluindo dados do cliente, transportadora e remetente.

## Criando o ambiente dev

1- Clonar o projeto

2- Montar o container
```bash
docker-compose up -d
```

3- Acessar o projeto:
```bash
http://localhost:9000
```
