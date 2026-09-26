# Modelo de dados previsto

Esta é uma visão inicial da estrutura de persistência, sujeita à validação dos requisitos. Nenhum banco de dados foi escolhido ou criado, e esta etapa não inclui SQL.

## Possíveis tabelas futuras

```text
clientes
profissionais
servicos
agendamentos
```

| Tabela prevista | Chave primária sugerida | Informações principais |
|---|---|---|
| clientes | id | nome, telefone, email |
| profissionais | id | nome, telefone, email, especialidade |
| servicos | id | nome, descricao, preco, duracao |
| agendamentos | id | data, horario, status e referências às demais tabelas |

## Chaves estrangeiras previstas

```text
agendamentos
- cliente_id
- profissional_id
- servico_id
```

| Campo em agendamentos | Referência prevista | Significado |
|---|---|---|
| cliente_id | clientes.id | Cliente do agendamento |
| profissional_id | profissionais.id | Profissional responsável |
| servico_id | servicos.id | Serviço agendado |

Cada agendamento deverá estar associado a exatamente um registro de cada uma dessas tabelas. Um cliente, profissional ou serviço poderá estar associado a zero ou mais agendamentos.

Os atributos e tipos Java sugeridos estão em [dados](../docs/dados.md). A persistência de Usuario e Administrador, incluindo o eventual mapeamento de herança, será definida posteriormente. Esta proposta não determina o banco, framework ou mecanismo de acesso aos dados.
