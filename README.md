# PataAmiga

> Plataforma web de gestão para ONGs de resgate e adoção de animais.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>PataAmiga</b> é uma plataforma web desenvolvida para centralizar e otimizar a gestão de ONGs dedicadas ao resgate e adoção de animais. O sistema acompanha o ciclo de vida completo de cada animal — desde o resgate inicial, passando pelos cuidados veterinários, até a adoção responsável — integrando todos os atores envolvidos: adotantes, voluntários, veterinários, coordenadores e doadores em uma única solução.
      </div>
    </td>
    <td>
      <div align="center">
        <!-- TODO: adicionar logo do PataAmiga -->
        🐾
      </div>
    </td>
  </tr>
</table>

---

## Status do Projeto

[![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue?style=for-the-badge)](https://github.com/RenatoDNS/PataAmiga/releases)
![Java](https://img.shields.io/badge/Java-21-007ec6?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-007ec6?style=for-the-badge&logo=springboot&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-17-007ec6?style=for-the-badge&logo=angular&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Compose-007ec6?style=for-the-badge&logo=docker&logoColor=white)
[![Licença](https://img.shields.io/github/license/RenatoDNS/PataAmiga?style=for-the-badge)](#licença)

---

## Índice

- [Links Úteis](#links-úteis)
- [Sobre o Projeto](#sobre-o-projeto)
- [Atores do Sistema](#atores-do-sistema)
- [Funcionalidades Principais](#funcionalidades-principais)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Arquitetura](#arquitetura)
  - [Diagrama de Casos de Uso](#diagrama-de-casos-de-uso)
  - [Diagrama de Classes e Pacotes](#diagrama-de-classes-e-pacotes)
  - [Diagrama Entidade-Relacionamento](#diagrama-entidade-relacionamento)
  - [Diagramas de Sequência](#diagramas-de-sequência)
  - [Diagrama de Atividade](#diagrama-de-atividade)
  - [Diagrama de Estado](#diagrama-de-estado)
  - [Diagrama de Componentes](#diagrama-de-componentes)
  - [Diagrama de Implantação](#diagrama-de-implantação)
- [Instalação e Execução](#instalação-e-execução)
- [Estrutura de Pastas](#estrutura-de-pastas)
- [Documentações Utilizadas](#documentações-utilizadas)
- [Autores](#autores)
- [Agradecimentos](#agradecimentos)
- [Licença](#licença)

---

## Links Úteis

- 📖 **PlantUML:** [Documentação Oficial](https://plantuml.com)
- 📖 **Spring Boot:** [Referência](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- 📖 **Angular:** [Documentação Oficial](https://angular.dev)
- 📖 **Conventional Commits:** [Guia de Mensagens](https://www.conventionalcommits.org/en/v1.0.0/)

---

## Sobre o Projeto

ONGs de resgate e adoção de animais frequentemente operam com processos manuais e descentralizados — planilhas, grupos de WhatsApp e cadernos físicos — o que dificulta o controle, compromete a rastreabilidade e limita a capacidade de atendimento.

O **PataAmiga** resolve esse problema oferecendo uma plataforma centralizada que:

- Registra e acompanha cada animal desde o resgate até a adoção
- Organiza o histórico veterinário completo de cada animal
- Gerencia o processo de adoção com etapas formalizadas
- Conecta adotantes a animais disponíveis com busca por perfil
- Permite que doadores acompanhem o impacto de suas contribuições
- Fornece ao coordenador da ONG visibilidade operacional e relatórios gerenciais

---

> **Contexto Acadêmico**
>
> Este projeto é o **Trabalho 2** da disciplina de **Projeto de Software** da **PUC Minas** (Prof. Dr. João Paulo Aramuni). O trabalho solicita a **documentação arquitetural completa** de um sistema de software — incluindo especificação de requisitos, modelagem UML com PlantUML, definição de tecnologias e descrição da arquitetura.
>
> **Este repositório contém exclusivamente documentação.** Não há código-fonte implementado. A estrutura de pastas apresentada na seção [Estrutura de Pastas](#estrutura-de-pastas) representa como o projeto seria organizado caso fosse desenvolvido, servindo como artefato de projeto de software.

---

## Atores do Sistema

| Ator | Tipo | Responsabilidades |
|------|------|-------------------|
| **Adotante** | Externo | Buscar animais disponíveis, submeter solicitação de adoção, acompanhar o processo e registrar pós-adoção |
| **Voluntário** | Interno | Registrar animais resgatados, agendar atendimentos veterinários, atualizar status e apoiar eventos |
| **Veterinário** | Interno | Emitir laudos clínicos, registrar prontuários, aplicar vacinas e procedimentos, liberar animais para adoção |
| **Coordenador da ONG** | Interno | Gerenciar equipe, aprovar ou rejeitar adoções, controlar recursos, emitir relatórios gerenciais |
| **Doador** | Externo | Realizar doações pontuais ou recorrentes, acompanhar uso dos recursos e visualizar relatórios de impacto |

---

## Funcionalidades Principais

- **Gestão de Animais:** Cadastro completo com foto, espécie, raça, idade, porte e acompanhamento de status ao longo do ciclo de vida
- **Prontuário Veterinário:** Registro de consultas, vacinas, procedimentos cirúrgicos e laudos de liberação para adoção
- **Processo de Adoção:** Fluxo formalizado — solicitação → entrevista → aprovação → contrato → acompanhamento pós-adoção
- **Busca e Filtragem:** Adotantes podem filtrar animais por espécie, porte, idade, sexo e localidade
- **Gestão de Voluntários:** Cadastro, disponibilidade, alocação de tarefas e histórico de atividades
- **Gestão de Doações:** Registro de doadores, histórico de doações, comprovantes e relatório de destinação
- **Painel do Coordenador:** Visão gerencial com indicadores de animais, adoções e recursos em tempo real
- **Notificações:** Alertas para adotantes sobre atualização de status e para voluntários sobre agendamentos

---

## Tecnologias Utilizadas

### Frontend

- **Framework:** Angular 17
- **Linguagem:** TypeScript
- **Estilização:** Angular Material / Tailwind CSS
- **Gerenciamento de Estado:** NgRx / Angular Signals
- **HTTP:** Angular HttpClient

### Backend

- **Linguagem:** Java 21
- **Framework:** Spring Boot 3.x
- **Banco de Dados:** PostgreSQL 16
- **ORM:** Hibernate / JPA
- **Autenticação:** JWT + Spring Security
- **Build:** Maven

### Infraestrutura

- **Containerização:** Docker + Docker Compose
- **CI/CD:** GitHub Actions

---

## Arquitetura

O PataAmiga adota uma arquitetura **monolítica modular em camadas**, adequada para o porte de uma ONG de pequeno e médio porte. O sistema é dividido em três grandes blocos: frontend Angular (SPA), backend Spring Boot (API REST) e banco de dados PostgreSQL — todos orquestrados via Docker Compose.

**Pacotes do backend (`br.pucminas.pataamiga`):**

```
controller/          — @RestController, mapeamento de rotas REST
service/             — @Service, regras de negócio
repository/          — interfaces Spring Data JPA (@Repository)
model/               — entidades JPA (@Entity, @Table)
dto/
  ├── request/       — payloads de entrada (AnimalRequestDTO…)
  └── response/      — payloads de saída  (AnimalResponseDTO…)
mapper/              — conversão DTO ↔ Entity via MapStruct (@Mapper)
exception/           — exceptions customizadas + @RestControllerAdvice
config/              — SecurityConfig, OpenApiConfig, CorsConfig
security/            — JwtFilter, JwtUtil, UserDetailsServiceImpl
```

**Padrões adotados:** Repository Pattern, Service Layer, DTO (request/response), Mapper (MapStruct), Global Exception Handling, Spring Security com RBAC por perfil de ator.

Os diagramas a seguir detalham cada aspecto da arquitetura.

---

### Diagrama de Casos de Uso

> Visão geral das interações entre os 5 atores e as funcionalidades do sistema.

<!-- TODO: inserir imagem -->
| Casos de Uso |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/01-caso-de-uso.puml`](docs/diagrams/puml/01-caso-de-uso.puml)

---

### Diagrama de Classes e Pacotes

> Modelo de domínio com entidades, atributos, métodos, relacionamentos e organização em pacotes do backend.

<!-- TODO: inserir imagem -->
| Classes e Pacotes |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/02-classes-e-pacotes.puml`](docs/diagrams/puml/02-classes-e-pacotes.puml)

---

### Diagrama Entidade-Relacionamento

> Esquema relacional do banco de dados PostgreSQL com tabelas, chaves e cardinalidades.

<!-- TODO: inserir imagem -->
| Entidade-Relacionamento |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/03-entidade-relacionamento.puml`](docs/diagrams/puml/03-entidade-relacionamento.puml)

---

### Diagramas de Sequência

> Interações passo a passo entre atores e componentes nos principais fluxos do sistema.

<!-- TODO: inserir imagens -->
| Processo de Adoção | Entrada de Animal Resgatado |
| :---: | :---: |
| _Em desenvolvimento_ | _Em desenvolvimento_ |

Fontes PlantUML:
- [`docs/diagrams/puml/04-sequencia-adocao.puml`](docs/diagrams/puml/04-sequencia-adocao.puml)
- [`docs/diagrams/puml/05-sequencia-entrada-animal.puml`](docs/diagrams/puml/05-sequencia-entrada-animal.puml)

---

### Diagrama de Atividade

> Fluxo de decisões e etapas do processo de adoção, do ponto de vista do sistema.

<!-- TODO: inserir imagem -->
| Atividade — Fluxo de Adoção |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/06-atividade-adocao.puml`](docs/diagrams/puml/06-atividade-adocao.puml)

---

### Diagrama de Estado

> Ciclo de vida de um animal dentro da plataforma, do resgate à adoção.

<!-- TODO: inserir imagem -->
| Estados do Animal |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/07-estado-animal.puml`](docs/diagrams/puml/07-estado-animal.puml)

---

### Diagrama de Componentes

> Estrutura interna do sistema com módulos, interfaces e dependências.

<!-- TODO: inserir imagem -->
| Componentes do Sistema |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/08-componentes.puml`](docs/diagrams/puml/08-componentes.puml)

---

### Diagrama de Implantação

> Infraestrutura física/virtual — containers Docker, redes e serviços.

<!-- TODO: inserir imagem -->
| Infraestrutura de Implantação |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/09-implantacao.puml`](docs/diagrams/puml/09-implantacao.puml)

---

## Instalação e Execução

### Pré-requisitos

- **Java JDK 21** ou superior
- **Node.js** LTS (v18 ou superior) + **Angular CLI** (`npm install -g @angular/cli`)
- **Docker** e **Docker Compose**

### Execução com Docker Compose

```bash
git clone https://github.com/RenatoDNS/PataAmiga.git
cd PataAmiga
docker-compose up --build -d
```

Acesse em: `http://localhost:4200` (frontend) e `http://localhost:8080/api` (backend)

### Execução Manual

```bash
# Backend
cd backend
./mvnw spring-boot:run

# Frontend (outro terminal)
cd frontend
npm install
ng serve
```

### Variáveis de Ambiente

| Variável | Descrição | Padrão |
|----------|-----------|--------|
| `SPRING_DATASOURCE_URL` | URL do PostgreSQL | `jdbc:postgresql://localhost:5432/pataamiga` |
| `SPRING_DATASOURCE_USERNAME` | Usuário do banco | `postgres` |
| `SPRING_DATASOURCE_PASSWORD` | Senha do banco | — |
| `JWT_SECRET` | Chave de assinatura JWT | — |
| `apiUrl` (environment.ts) | URL base da API | `http://localhost:8080/api` |

---

## Estrutura de Pastas

```
PataAmiga/
├── .github/
│   └── workflows/              # CI/CD com GitHub Actions
├── docs/
│   └── diagrams/
│       ├── puml/               # Fontes PlantUML (10 diagramas)
│       └── png/                # Imagens geradas dos diagramas
├── backend/                    # API Spring Boot (Java 21)
│   └── src/main/java/
│       └── br/pucminas/pataamiga/
│           ├── controller/     # @RestController — endpoints REST
│           ├── service/        # @Service — regras de negócio
│           ├── repository/     # Spring Data JPA
│           ├── model/          # @Entity — entidades JPA
│           ├── dto/
│           │   ├── request/    # payloads de entrada
│           │   └── response/   # payloads de saída
│           ├── mapper/         # MapStruct — DTO ↔ Entity
│           ├── exception/      # exceptions + @RestControllerAdvice
│           ├── config/         # SecurityConfig, OpenApiConfig, CorsConfig
│           └── security/       # JwtFilter, JwtUtil, UserDetailsServiceImpl
├── frontend/                   # SPA Angular 17 + TypeScript
│   └── src/app/
│       ├── core/               # Guards, interceptors, serviços singleton
│       ├── shared/             # Componentes e pipes reutilizáveis
│       ├── features/           # Módulos por funcionalidade
│       │   ├── animal/
│       │   ├── adocao/
│       │   ├── veterinario/
│       │   └── doador/
│       └── layout/             # Header, footer, navegação
├── docker-compose.yml
├── LICENSE
└── README.md
```

---

## Documentações Utilizadas

- [PlantUML — Documentação Oficial](https://plantuml.com)
- [PlantUML Language Reference Guide (PDF)](https://plantuml.com/guide)
- [Spring Boot — Referência](https://docs.spring.io/spring-boot/docs/current/reference/html/)
- [Angular — Documentação Oficial](https://angular.dev)
- [MapStruct — Referência](https://mapstruct.org/documentation/stable/reference/html/)
- [Docker — Documentação de Referência](https://docs.docker.com/)
- [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

## Autores

| Nome | GitHub | LinkedIn |
|------|--------|----------|
| Renato Douglas | [RenatoDNS](https://github.com/RenatoDNS) | [renatodns](https://www.linkedin.com/in/renatodns/) |

---

## Agradecimentos

- [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo suporte institucional e estrutura acadêmica
- [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos em Arquitetura de Software e Padrões de Projeto

---

## Licença

Este projeto é distribuído sob a [Licença MIT](./LICENSE).
