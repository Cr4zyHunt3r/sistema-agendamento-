# Arquitetura inicial

A proposta inicial é uma arquitetura em camadas, simples e adequada a um projeto acadêmico em Java. A separação de responsabilidades facilita a compreensão e a manutenção do sistema.

## Camada de Apresentação

Responsável pela interação com o usuário, apresentando informações e recebendo entradas. A tecnologia de interface será definida durante o desenvolvimento.

## Camada de Controle

Responsável por receber ações da interface e encaminhá-las para as regras do sistema. Os controllers também devolvem os resultados para a apresentação.

## Camada de Serviço / Regras de Negócio

Responsável por:

- Verificar disponibilidade.
- Validar agendamentos.
- Evitar conflitos de horário.
- Controlar cancelamentos.

As regras serão detalhadas após o levantamento de requisitos, considerando a duração dos serviços e a agenda dos profissionais.

## Camada de Persistência

Responsável pela comunicação com o banco de dados por meio de repositories. O banco de dados e a forma de persistência serão definidos posteriormente; nesta entrega há apenas a documentação do modelo previsto.

## Camada de Modelo

Responsável pelas entidades principais do domínio, como Cliente, Profissional, Servico e Agendamento. Essas entidades representam os dados e comportamentos do domínio e são utilizadas pelas demais camadas conforme necessário.

## Fluxo inicial

```text
Interface
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
Banco de Dados
```

O fluxo representa o encaminhamento de uma solicitação até a persistência; os resultados retornam às camadas anteriores. O modelo apoia essas interações e não representa uma etapa adicional depois do banco de dados.

Esta arquitetura poderá ser ajustada posteriormente. Nenhum framework foi escolhido. A estrutura de pacotes Java será definida quando a arquitetura estiver validada.
