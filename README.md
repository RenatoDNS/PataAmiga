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
- [Funcionalidades Principais](#funcionalidades-principais)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [2. Modelos de Usuário e Requisitos](#2-modelos-de-usuário-e-requisitos)
  - [2.1 Descrição de Atores](#21-descrição-de-atores)
  - [2.2 Modelo de Casos de Uso](#22-modelo-de-casos-de-uso)
  - [2.3 Diagramas de Sequência do Sistema e Contratos de Operações](#23-diagramas-de-sequência-do-sistema-e-contratos-de-operações)
- [3. Modelos de Projeto](#3-modelos-de-projeto)
  - [3.1 Arquitetura (C4 Model)](#31-arquitetura-c4-model)
  - [3.2 Diagrama de Componentes e Implantação](#32-diagrama-de-componentes-e-implantação)
  - [3.3 Diagrama de Classes](#33-diagrama-de-classes)
  - [3.4 Diagramas de Sequência](#34-diagramas-de-sequência)
  - [3.5 Diagramas de Comunicação](#35-diagramas-de-comunicação)
  - [3.6 Diagrama de Estados](#36-diagrama-de-estados)
- [4. Modelos de Dados](#4-modelos-de-dados)
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

## 2. Modelos de Usuário e Requisitos

### 2.1 Descrição de Atores

| Ator | Tipo | Responsabilidades |
|------|------|-------------------|
| **Adotante** | Externo / Primário | Buscar animais disponíveis, submeter solicitação de adoção, acompanhar o processo e registrar pós-adoção |
| **Voluntário** | Interno / Operacional | Registrar animais resgatados, agendar atendimentos veterinários, atualizar status e apoiar eventos |
| **Veterinário** | Interno / Especialista | Emitir laudos clínicos, registrar prontuários, aplicar vacinas e procedimentos, liberar animais para adoção |
| **Coordenador da ONG** | Interno / Administrativo | Gerenciar equipe, aprovar ou rejeitar adoções, controlar recursos, emitir relatórios gerenciais |
| **Doador** | Externo / Suporte | Realizar doações pontuais ou recorrentes, acompanhar uso dos recursos e visualizar relatórios de impacto |

---

### 2.2 Modelo de Casos de Uso

> Visão geral das interações entre os 5 atores e as funcionalidades do sistema. Cada caso de uso recebe um ID (`UC-NN`) usado como referência cruzada nas demais seções.

#### Lista de Casos de Uso

Os 14 casos de uso estão agrupados em 5 pacotes funcionais.

| ID | Caso de Uso | Ator(es) Primário(s) | Pacote |
|----|-------------|---------------------|--------|
| **UC-01** | Solicitar Adoção | Adotante | Adoção |
| **UC-02** | Registrar Animal Resgatado | Voluntário | Gestão de Animais |
| **UC-03** | Registrar Atendimento Veterinário | Veterinário | Atendimento Veterinário |
| **UC-04** | Buscar Animal Disponível | Adotante | Adoção |
| **UC-05** | Acompanhar Processo de Adoção | Adotante | Adoção |
| **UC-06** | Registrar Pós-Adoção | Adotante | Adoção |
| **UC-07** | Atualizar Status do Animal | Voluntário | Gestão de Animais |
| **UC-08** | Agendar Atendimento Veterinário | Voluntário | Gestão de Animais |
| **UC-09** | Emitir Laudo de Liberação para Adoção | Veterinário | Atendimento Veterinário |
| **UC-10** | Aprovar/Rejeitar Adoção | Coordenador da ONG | Adoção |
| **UC-11** | Gerenciar Voluntários | Coordenador da ONG | Administração |
| **UC-12** | Emitir Relatórios Gerenciais | Coordenador da ONG | Administração |
| **UC-13** | Realizar Doação | Doador | Doações |
| **UC-14** | Acompanhar Destinação das Doações | Doador | Doações |

#### Relacionamentos entre Casos de Uso

| Relacionamento | Descrição |
|---|---|
| `UC-03` **«include»** `UC-07` | Todo atendimento veterinário registra uma transição de status (ex.: `RESGATADO` → `EM_TRATAMENTO`). |
| `UC-09` **«include»** `UC-07` | A emissão do laudo de liberação move o animal para `DISPONIVEL`. |
| `UC-10` **«include»** `UC-07` | A aprovação move para `EM_PROCESSO_ADOCAO`/`ADOTADO`; a rejeição mantém em `DISPONIVEL`. |

| ![Diagrama de Casos de Uso](docs/diagrams/png/01-caso-de-uso.png) |
| :---: |
| **Figura 1** — Diagrama de Casos de Uso do PataAmiga |

Fonte PlantUML: [`docs/diagrams/puml/01-caso-de-uso.puml`](docs/diagrams/puml/01-caso-de-uso.puml)

---

### 2.3 Diagramas de Sequência do Sistema e Contratos de Operações

> Diagramas de Sequência do Sistema (SSD) — visão **caixa-preta** das três operações de sistema escolhidas. Cada SSD origina um **contrato de operação** com pré-condições e pós-condições.

<!-- TODO: inserir imagens -->
| UC-01 Solicitar Adoção | UC-02 Registrar Animal | UC-03 Registrar Atendimento |
| :---: | :---: | :---: |
| _Em desenvolvimento_ | _Em desenvolvimento_ | _Em desenvolvimento_ |

Fontes PlantUML:
- [`docs/diagrams/puml/02-ssd-solicitar-adocao.puml`](docs/diagrams/puml/02-ssd-solicitar-adocao.puml)
- [`docs/diagrams/puml/03-ssd-registrar-animal.puml`](docs/diagrams/puml/03-ssd-registrar-animal.puml)
- [`docs/diagrams/puml/04-ssd-registrar-atendimento.puml`](docs/diagrams/puml/04-ssd-registrar-atendimento.puml)

#### Contratos de Operação

> _Em desenvolvimento — um contrato por operação de sistema chave (Operação · Referências cruzadas · Pré-condições · Pós-condições)._

---

## 3. Modelos de Projeto

### 3.1 Arquitetura (C4 Model)

O PataAmiga adota uma arquitetura **monolítica modular em camadas**, adequada para o porte de uma ONG de pequeno e médio porte. A arquitetura é apresentada em três níveis do **C4 Model**: contexto, containers e componentes.

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

#### C4 Nível 1 — Contexto

<!-- TODO: inserir imagem -->
| Contexto |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/05-c4-contexto.puml`](docs/diagrams/puml/05-c4-contexto.puml)

#### C4 Nível 2 — Containers

<!-- TODO: inserir imagem -->
| Containers |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/06-c4-containers.puml`](docs/diagrams/puml/06-c4-containers.puml)

---

### 3.2 Diagrama de Componentes e Implantação

> O **diagrama de componentes** é o **C4 Nível 3**, detalhando os componentes internos do backend. O **diagrama de implantação** mostra onde cada container é alocado na infraestrutura Docker.

#### Diagrama de Componentes (C4 Nível 3)

<!-- TODO: inserir imagem -->
| Componentes do Backend |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/07-c4-componentes.puml`](docs/diagrams/puml/07-c4-componentes.puml)

#### Diagrama de Implantação

<!-- TODO: inserir imagem -->
| Infraestrutura de Implantação |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/08-implantacao.puml`](docs/diagrams/puml/08-implantacao.puml)

---

### 3.3 Diagrama de Classes

> Modelo de domínio com entidades, atributos, métodos e relacionamentos.

<!-- TODO: inserir imagem -->
| Classes do Domínio |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/09-classes.puml`](docs/diagrams/puml/09-classes.puml)

---

### 3.4 Diagramas de Sequência

> Realização interna (caixa-branca) de cada caso de uso — atores, controllers, services, repositórios e banco.

<!-- TODO: inserir imagens -->
| UC-01 Solicitar Adoção | UC-02 Registrar Animal | UC-03 Registrar Atendimento |
| :---: | :---: | :---: |
| _Em desenvolvimento_ | _Em desenvolvimento_ | _Em desenvolvimento_ |

Fontes PlantUML:
- [`docs/diagrams/puml/10-seq-solicitar-adocao.puml`](docs/diagrams/puml/10-seq-solicitar-adocao.puml)
- [`docs/diagrams/puml/11-seq-registrar-animal.puml`](docs/diagrams/puml/11-seq-registrar-animal.puml)
- [`docs/diagrams/puml/12-seq-registrar-atendimento.puml`](docs/diagrams/puml/12-seq-registrar-atendimento.puml)

---

### 3.5 Diagramas de Comunicação

> Mesmas mensagens dos diagramas de sequência da seção 3.4, vistas como **colaboração entre objetos** (numeração sobre as conexões).

<!-- TODO: inserir imagens -->
| UC-01 Solicitar Adoção | UC-02 Registrar Animal | UC-03 Registrar Atendimento |
| :---: | :---: | :---: |
| _Em desenvolvimento_ | _Em desenvolvimento_ | _Em desenvolvimento_ |

Fontes PlantUML:
- [`docs/diagrams/puml/13-com-solicitar-adocao.puml`](docs/diagrams/puml/13-com-solicitar-adocao.puml)
- [`docs/diagrams/puml/14-com-registrar-animal.puml`](docs/diagrams/puml/14-com-registrar-animal.puml)
- [`docs/diagrams/puml/15-com-registrar-atendimento.puml`](docs/diagrams/puml/15-com-registrar-atendimento.puml)

---

### 3.6 Diagrama de Estados

> Ciclo de vida de um animal dentro da plataforma, do resgate à adoção (`RESGATADO` → `EM_TRATAMENTO` → `DISPONIVEL` → `EM_PROCESSO_ADOCAO` → `ADOTADO` / `OBITO`).

<!-- TODO: inserir imagem -->
| Estados do Animal |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/16-estado-animal.puml`](docs/diagrams/puml/16-estado-animal.puml)

---

## 4. Modelos de Dados

> Esquema relacional do banco PostgreSQL e a estratégia de mapeamento objeto/relacional adotada (Hibernate/JPA).

### Diagrama Entidade-Relacionamento

<!-- TODO: inserir imagem -->
| Entidade-Relacionamento |
| :---: |
| _Em desenvolvimento_ |

Fonte PlantUML: [`docs/diagrams/puml/17-entidade-relacionamento.puml`](docs/diagrams/puml/17-entidade-relacionamento.puml)

### Estratégia de Mapeamento Objeto-Relacional

> _Em desenvolvimento — descreverá como entidades JPA são mapeadas para tabelas (`@Entity`, `@Table`, `@Id`/`@GeneratedValue`, relacionamentos `@OneToMany` / `@ManyToOne`, estratégia de herança quando aplicável, e enums como `@Enumerated(EnumType.STRING)`)._

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
│       ├── puml/               # Fontes PlantUML (17 diagramas)
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
