# Teste de back-end TempoCerto

Este teste busca avaliar quesitos técnicos para as pessoas que se candidatem às vagas de desenvolvimento back-end da TempoCerto.

## O desafio

O objetivo é criar endpoints para que possamos simular:

## 1. Solicitar agendamento:

### Esse endpoint deve receber os seguintes dados:

> [POST] /agendas

```json
{
    "empresa": {
        "cnpj": "26488705000193"
    },
    "horario": "10:00",
}
```

## 2. Listar agendas:

### Esse endpoint deve retornar os seguintes dados:

##### `Lista de agendas atuais solicitadas`

> [GET] /agendas
```json
[
    {
        "horario": "10:00",
        "empresa": {
            "cnpj":"26488705000193",
            ...
        },
    },
]
```

## 3. Verificar disponibilidade de horários:

### Esse endpoint deve retornar os seguintes dados:
##### `Lista de horários (dentro do período de 8h até às 18h quais horários estão disponíveis com intervalo fixo de 1 hora)`
> [GET] /agendas:disponibilidade
```json
[
    {
        "inicio":"8:00",
        "fim":"9:00",
        "disponivel": true,
    },
    {
        "inicio":"9:00",
        "fim":"10:00",
        "disponivel": false,
    },
    ...
]
```


## Requisitos
- [Golang](https://go.dev/)

### Desejável (Será considerado um diferencial)

- Uso da API [Receita WS](https://developers.receitaws.com.br/#/operations/queryCNPJFree) para consultar o cnpj e trazer a razão social da empresa na rota de listagem das agendas.

## O que será avaliado

- Utilização correta de git
- Código limpo e organizado (nomenclatura, etc)
- Modelagem de Dados
- Tratamento de erros
- Arquitetura
- README.md bem escrito, curto e com os comandos necessários para rodar a aplicação, bastando copiar/colar no terminal.

