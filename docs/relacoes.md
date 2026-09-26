# Relações iniciais entre entidades

```text
Cliente 1 -------- N Agendamento

Profissional 1 --- N Agendamento

Servico 1 -------- N Agendamento
```

- Um cliente pode realizar vários agendamentos.
- Um profissional pode possuir vários agendamentos.
- Um serviço pode estar presente em vários agendamentos.
- Cada agendamento deve possuir exatamente um cliente.
- Cada agendamento deve possuir exatamente um profissional.
- Cada agendamento deve possuir exatamente um serviço.

Neste modelo, `N` significa zero ou mais: clientes, profissionais e serviços podem estar cadastrados sem possuir agendamentos. As associações obrigatórias estão no Agendamento.

## Possibilidade futura de herança

```text
Usuario
├── Cliente
├── Profissional
└── Administrador
```

Essa estrutura pode permitir a utilização de herança na aplicação, concentrando os atributos comuns em Usuario. Trata-se de uma possibilidade inicial, a ser validada após o levantamento de requisitos, e não de uma implementação já realizada.

A organização das classes por herança não define automaticamente a organização das tabelas do banco. O mapeamento de persistência será decidido posteriormente.
