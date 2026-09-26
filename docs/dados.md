# Estrutura inicial dos dados

Os tipos abaixo são sugestões iniciais para Java e poderão ser alterados após a validação dos requisitos. Não representam a definição de um banco de dados ou de tipos SQL.

## Cliente

| Campo | Tipo sugerido | Descrição |
|---|---|---|
| id | Long/Integer | Identificador do cliente |
| nome | String | Nome completo |
| telefone | String | Telefone, preservando formatação e zeros iniciais |
| email | String | E-mail |

## Profissional

| Campo | Tipo sugerido | Descrição |
|---|---|---|
| id | Long/Integer | Identificador do profissional |
| nome | String | Nome completo |
| telefone | String | Telefone |
| email | String | E-mail |
| especialidade | String | Especialidade do profissional |

## Serviço (Servico)

| Campo | Tipo sugerido | Descrição |
|---|---|---|
| id | Long/Integer | Identificador do serviço |
| nome | String | Nome do serviço |
| descricao | String | Descrição do serviço oferecido |
| preco | BigDecimal | Valor monetário do serviço |
| duracao | Integer | Duração prevista em minutos |

## Agendamento

| Campo | Tipo sugerido | Descrição |
|---|---|---|
| id | Long/Integer | Identificador do agendamento |
| data | LocalDate | Data do atendimento |
| horario | LocalTime | Horário de início do atendimento |
| status | Enum a definir | Situação do agendamento; valores e transições serão validados posteriormente |
| cliente | Cliente | Referência ao único cliente associado |
| profissional | Profissional | Referência ao único profissional associado |
| servico | Servico | Referência ao único serviço associado |

As referências representam associações entre objetos. No modelo de persistência previsto, poderão corresponder a chaves estrangeiras, conforme [modelo de dados](../database/modelo-dados.md).

Se a classe base Usuario for adotada, seus dados comuns serão `id`, `nome`, `telefone` e `email`, com os mesmos tipos sugeridos acima. Os dados específicos de Administrador serão definidos posteriormente.
