# Entidades iniciais

## Usuario

Atributos:

- `id`
- `nome`
- `telefone`
- `email`

Poderá ser utilizada como classe base para reunir atributos comuns de Cliente, Profissional e Administrador. A adoção de herança ainda será avaliada.

## Cliente

Atributos iniciais:

- `id`
- `nome`
- `telefone`
- `email`

Responsabilidade: realizar e acompanhar agendamentos.

## Profissional

Atributos:

- `id`
- `nome`
- `telefone`
- `email`
- `especialidade`

Responsabilidade: realizar os serviços e possuir uma agenda de atendimentos.

## Servico

Atributos:

- `id`
- `nome`
- `descricao`
- `preco`
- `duracao`

Responsabilidade: representar um serviço disponibilizado pelo estabelecimento. A duração será inicialmente expressa em minutos.

## Agendamento

Atributos:

- `id`
- `data`
- `horario`
- `status`
- `cliente`
- `profissional`
- `servico`

Responsabilidade: representar o agendamento de um serviço, associando exatamente um cliente, um profissional e um serviço a uma data e horário.

## Administrador

Responsabilidade: gerenciar profissionais, serviços e informações do estabelecimento. Seus atributos específicos serão definidos no levantamento de requisitos; caso a herança seja adotada, poderá receber os atributos comuns de Usuario.

## Evolução do modelo

As entidades ainda poderão sofrer alterações após o levantamento de requisitos. Os atributos comuns foram listados em Cliente e Profissional para facilitar a leitura; caso Usuario se torne uma classe base, esses atributos poderão ser herdados, sem duplicação na implementação.
