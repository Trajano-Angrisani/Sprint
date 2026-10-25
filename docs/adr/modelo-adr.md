# ADR-001 Escolha da Solução de Arquitetura e Stack

- **Situação:** aceita
- **Data:** 2026-10-24
- **Participantes:** Bernardo, <Nome do Colega 2>, <Nome do Colega 3>

## Contexto

Precisamos definir a stack tecnológica e a solução de arquitetura inicial para o desenvolvimento do projeto Connexa. Devemos garantir suporte para banco de dados relacional, facilitar a comunicação entre o front-end e a API do back-end, e respeitar o prazo do projeto considerando o conhecimento prévio e a experiência técnica da equipe.

## Decisão

Adotamos a stack **Java (Spring Boot)** para o desenvolvimento do back-end, **React (Vite)** para o front-end e **PostgreSQL** como banco de dados relacional.

## Alternativas consideradas

| Alternativa | Por que não foi escolhida |
|---|---|
| Node.js / Express | A equipe possui maior curva de aprendizado e prefere a estrutura tipada e padronizada do Java com Spring Boot. |
| .NET (C#) | Apesar de robusto, a equipe tem mais familiaridade com o ecossistema Java para este projeto. |

## Consequências

- **Positivas:** Framework amplamente documentado, facilidade de integração com Spring Data JPA para persistência de dados e ambiente front-end ágil com Vite.
- **Negativas:** Maior verbosidade nas configurações e necessidade de gerenciar o consumo de recursos na execução paralela do back-end e front-end.
- **Como verificar:** Execução dos testes automatizados via script `./verificar`, inicialização com sucesso da aplicação via `spring-boot:run` e `npm run dev`, além do build do CI no GitHub Actions.
