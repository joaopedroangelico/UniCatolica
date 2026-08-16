# AcadêmicoHub

Rede social acadêmica da UniCatólica — permite que estudantes, professores e a
coordenação compartilhem conteúdo e interajam em um feed voltado à vida
acadêmica.

## Integrantes e responsabilidades

| Integrante | Frente principal |
|---|---|
| João Pedro Angélico | *A DEFINIR* |
| Gustavo Taques | *A DEFINIR* |
| Luis Fernando | *A DEFINIR* |
| Vynicyus Cândido | *A DEFINIR* |

> Responsável de comunicação com professor/parceiro: *A DEFINIR*

## Problema atendido e público beneficiado

A comunidade acadêmica da UniCatólica (estudantes, professores e coordenação)
não tem um espaço próprio e simples para compartilhar conteúdo acadêmico e
interagir. O AcadêmicoHub propõe uma rede social enxuta e voltada a esse
público.

## Objetivo do sistema

Permitir que estudantes criem perfil, publiquem posts acadêmicos e interajam
em um feed, com autenticação segura e uma base técnica que suporte evolução
ao longo do PAC VI.

## Stack tecnológica

| Frente | Tecnologia | Justificativa |
|---|---|---|
| Frontend | Angular | Reaproveita decisões de UI/roteamento da fase de proposta do PAC Extensionista |
| Backend | Java com Quarkus | Produtividade com CDI e bom desempenho em contêiner |
| Banco de dados | PostgreSQL | Robustez para dados relacionais (usuários, posts, perfis) |
| Autenticação/autorização | JWT | Padrão stateless, compatível com Angular + Quarkus |
| Hospedagem/deploy | *A DEFINIR* | |
| Testes | *A DEFINIR* | |
| CI/CD | *A DEFINIR* | |
| Gestão de tarefas | *A DEFINIR* | |
| Prototipação/design | *A DEFINIR* | |

## Arquitetura resumida

Arquitetura cliente-servidor em três camadas: SPA em Angular consumindo uma
API REST em Java/Quarkus, com persistência em PostgreSQL e autenticação via
JWT.

```
Frontend (Angular SPA)  --HTTP/REST(JSON)-->  Backend (Java/Quarkus API)
                                                    |-- PostgreSQL (dados)
                                                    '-- JWT (autenticação)
```

Diagrama completo: *A DEFINIR — sugestão: `/docs/arquitetura.png`*

## Instalação e execução local

### Frontend (Angular)

```bash
cd frontend
npm install
ng serve
```

Acesse em `http://localhost:4200`.

### Backend (Java/Quarkus)

```bash
cd backend
./mvnw quarkus:dev
```

API disponível em `http://localhost:8080`.

### Banco de dados (PostgreSQL)

*A DEFINIR — registrar aqui como subir o banco local (Docker Compose,
instância local, etc.) e a string de conexão usada em desenvolvimento.*

> Os comandos acima assumem a estrutura padrão de projeto Angular/Quarkus.
> Ajuste os caminhos (`frontend/`, `backend/`) conforme a estrutura real do
> repositório.

## Variáveis de ambiente

Ver `.env.example` na raiz de cada projeto (frontend/backend).

| Variável | Descrição |
|---|---|
| *A DEFINIR* | *A DEFINIR* |

## MVP

**Em uma frase:** permitir que estudantes da UniCatólica criem perfil,
publiquem posts acadêmicos e interajam em um feed simples.

- **Fluxo principal:** Login → Feed → Criar post → Ver perfil
- **Incluído no MVP:** cadastro/login (JWT), feed de posts, criação de post,
  perfil básico
- **Fora do MVP:** mensagens diretas, notificações push, moderação avançada,
  busca avançada

> Proposta inicial — validar com a equipe.

## Backlog

Backlog inicial (priorizado): ver [tabela no checkpoint](#) ou
`/docs/backlog.md` *(a definir onde ficará)*.

1. Estrutura inicial do repositório e README
2. Configuração do projeto Angular (frontend)
3. Configuração do projeto Quarkus + conexão PostgreSQL
4. Tela de login/cadastro
5. Endpoint de autenticação JWT
6. Feed de posts (listagem)
7. Criação de post
8. Tela de perfil básico

## Cronograma resumido

| Período | Marco |
|---|---|
| 10/08 a 24/08 | Ponto de partida mínimo concluído |
| 24/08 a 21/09 | Sprint 1 em desenvolvimento |
| 21/09 a 05/10 | Sprint 1 revisada e Sprint 2 planejada |
| 05/10 a 19/10 | Versão Alpha em implementação |
| 19/10 a 16/11 | Preparação para implementação/validação |
| Novembro | Implementação, validação e evolução da entrega |

## Próximos passos

- Definir responsáveis por frente (matriz de responsabilidades)
- Validar MVP, riscos e backlog com a equipe
- Configurar CI/CD, testes e ambiente de deploy
- Primeiro incremento funcional (Sprint 1)
