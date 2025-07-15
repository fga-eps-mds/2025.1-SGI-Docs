# Documento de Visão

## Histórico de Versão

| Data       | Versão | Descrição             | Autor(es)                          |
|------------|--------|---------------------|--------------------------------|
| 16/05/2025 | 1.0    | Adiciona do documento de visão | Danilo Domingo                 |

---

## Introdução

### Propósito
Este documento tem como objetivo definir em alto nível as necessidades e características do GitFica. O sistema visa incentivar o uso contínuo do GitHub por meio de elementos de gamificação. Este documento fornece uma visão geral das funcionalidades, restrições e características do sistema.

### Escopo
O GitFica é uma aplicação web que utiliza elementos de gamificação para incentivar e acompanhar o uso da plataforma GitHub. O sistema permite que os usuários visualizem e compartilhem seu progresso em atividades no GitHub (commits, issues, pull requests, etc.), ganhem pontos, subam de nível, conquistem badges e desafiem outros usuários.

### Definições, Acrônimos e Abreviações
* **MDS**: Métodos de Desenvolvimento de Software
* **EPS**: Engenharia de Produto de Software
* **PR**: Pull Request
* **MVP**: Minimum Viable Product (Produto Mínimo Viável)
* **UX**: User Experience (Experiência do Usuário)

### Referências
* [Backlog do produto](./backlog.md)
* [Sessão 1 - Lean Inception](./sessao-um-lean.md)
* [Sessão 2 - Lean Inception](./sessao-dois-lean.md)

## Posicionamento

### Oportunidade de Negócio
O GitHub é amplamente utilizado por equipes de desenvolvimento, mas muitas vezes há falta de engajamento contínuo dos membros. A gamificação tem se mostrado uma estratégia eficaz para aumentar o engajamento e a motivação em diversas áreas. O GitFica busca preencher essa lacuna, oferecendo uma plataforma que incentiva o uso regular e eficiente do GitHub através de mecânicas de jogos como pontos, níveis, missões e conquistas.

### Descrição do Problema

| Problema | Ausência de engajamento contínuo e organizado no uso do GitHub |
|----------|--------------------------------------------------------------|
| **Afeta** | Equipes de desenvolvimento de software, acadêmicos e profissionais |
| **Impacto** | Menor produtividade, colaboração inconsistente e dificuldade em manter padrões de qualidade no desenvolvimento |
| **Solução** | Um sistema que gamifique o uso do GitHub, transformando atividades de desenvolvimento em desafios, missões e conquistas, incentivando o engajamento contínuo |

## Descrição dos Envolvidos e dos Usuários

### Resumo dos Envolvidos

| Nome | Descrição | Responsabilidades |
|------|-----------|-------------------|
| Equipe de Desenvolvimento | Estudantes de MDS e EPS da Universidade de Brasília | Desenvolver, testar e implementar o sistema |
| Stakeholders | Professores e orientadores | Fornecer requisitos, avaliar entregas e orientar o desenvolvimento |

### Resumo dos Usuários

| Nome | Descrição | Responsabilidades |
|------|-----------|-------------------|
| Usuário Individual | Desenvolvedores que utilizam GitHub e desejam gamificar suas atividades | Utilizar o sistema, conectar sua conta GitHub, participar das missões e competições |
| Líderes de Equipe | Gerentes de projeto e líderes técnicos | Criar e gerenciar equipes, monitorar o desempenho da equipe |

### Ambiente do Usuário
Os usuários acessarão o sistema através de navegadores web em dispositivos desktop ou móveis. O usuário precisará ter uma conta ativa no GitHub para fazer login e utilizar as funcionalidades do sistema.

### Perfis dos Envolvidos

#### Equipe de Desenvolvimento
* **Representantes**: Estudantes de MDS e EPS
* **Descrição**: Responsáveis pelo desenvolvimento do sistema
* **Critérios de Sucesso**: Sistema implementado conforme requisitos, com alta qualidade e dentro do prazo estipulado
* **Envolvimento**: Alto

#### Stakeholders
* **Representantes**: Professores da disciplina
* **Descrição**: Orientadores do projeto e avaliadores do produto final
* **Critérios de Sucesso**: Sistema que atenda os requisitos educacionais e técnicos propostos
* **Envolvimento**: Médio

### Perfis dos Usuários

#### Usuário Individual
* **Descrição**: Desenvolvedores que utilizam GitHub regularmente
* **Responsabilidades**: Conectar sua conta GitHub, completar missões, ganhar pontos e conquistar badges
* **Critérios de Sucesso**: Aumento no engajamento com o GitHub e melhoria na produtividade
* **Comentários**: Principal usuário do sistema

#### Líderes de Equipe
* **Descrição**: Gerentes de projeto e líderes técnicos
* **Responsabilidades**: Criar e gerenciar equipes, visualizar métricas da equipe
* **Critérios de Sucesso**: Aumento na produtividade da equipe e melhoria na qualidade das entregas
* **Comentários**: Utilizará principalmente funcionalidades de gestão de equipe e relatórios

## Visão Geral do Produto

### Perspectiva do Produto
O GitFica é um sistema independente que se integra à API do GitHub para capturar e analisar as atividades dos usuários. A interface será web-based, responsiva e intuitiva, com elementos visuais que remetem a jogos para potencializar o envolvimento.

### Resumo das Capacidades

| Benefício para o Cliente | Recursos de Suporte |
|--------------------------|---------------------|
| Aumento do engajamento no GitHub | Sistema de pontuação baseado em atividades no GitHub |
| Visualização clara do progresso | Dashboard com métricas e estatísticas das atividades |
| Motivação contínua | Sistema de missões diárias, semanais e mensais |
| Reconhecimento de conquistas | Badges, níveis e prêmios virtuais por marcos alcançados |
| Espírito competitivo saudável | Rankings individuais e por equipes |
| Colaboração em equipe | Criação e gestão de equipes com objetivos compartilhados |

### Suposições e Dependências
* Os usuários possuem conta ativa no GitHub
* O GitHub mantém sua API disponível e com as funcionalidades atuais
* Os navegadores utilizados pelos usuários suportam as tecnologias empregadas no frontend

## Recursos do Produto

### Autenticação e Perfil de Usuário
* Login via GitHub
* Visualização e configuração de perfil
* Exclusão de conta

### Integração com GitHub
* Visualização de estatísticas de commits
* Visualização de issues cadastradas e finalizadas
* Acompanhamento de pull requests abertos, aceitos e rejeitados
* Contabilização de merges realizados

### Sistema de Gamificação
* Pontuação baseada em atividades no GitHub
* Sistema de níveis progressivos
* Conquistas e badges por objetivos alcançados
* Missões diárias, semanais e mensais

### Métricas e Estatísticas
* Dashboard com visualização de métricas individuais
* Gráficos e estatísticas de desempenho
* Histórico de pontos e atividades

### Sistema de Ranking
* Ranking individual entre todos os usuários
* Ranking por equipes
* Classificações por diferentes categorias (commits, PRs, etc.)

### Gestão de Equipes
* Criação e gestão de equipes
* Convites para novos membros
* Atribuição de papéis aos membros
* Visualização do desempenho da equipe

### Sistema de Notificações
* Alertas sobre missões cumpridas
* Notificações sobre conquistas
* Avisos sobre atividades da equipe

## Restrições

### Restrições de Design
* Interface responsiva para diferentes dispositivos
* Design intuitivo com elementos de gamificação
* Identidade visual coerente com o tema de gamificação

### Restrições de Implementação
* Desenvolvimento com arquitetura cliente-servidor
* Backend desenvolvido em Django Rest Framework
* Frontend desenvolvido em Next.js
* Utilização de Docker para containerização

### Restrições de Segurança
* Autenticação via OAuth do GitHub
* Proteção de dados sensíveis dos usuários
* Conformidade com práticas de segurança web

## Requisitos de Qualidade

### Usabilidade
* Interface intuitiva que não requer treinamento extensivo
* Tempo de resposta adequado para operações comuns
* Feedback claro para ações do usuário

### Confiabilidade
* Sistema disponível 24/7 com tempo de inatividade mínimo
* Recuperação adequada em caso de falhas
* Backup regular de dados críticos

### Desempenho
* Tempo de resposta rápido nas operações principais
* Capacidade de lidar com múltiplos usuários simultâneos
* Otimização para operações que envolvem consultas à API do GitHub

### Manutenibilidade
* Código bem documentado e seguindo padrões de qualidade
* Facilidade para implementação de novas funcionalidades
* Testes automatizados para garantir a qualidade

## Prioridades de Implementação

Com base no backlog do produto, as funcionalidades serão implementadas na seguinte ordem de prioridade:

* Sistema de autenticação via GitHub
* Visualização de métricas básicas (commits, issues, PRs)
* Sistema de pontuação
* Dashboard com estatísticas
* Sistema de missões e conquistas
* Ranking individual
* Gestão de equipes e ranking por equipes
* Sistema de notificações

## Conclusão

O GitFica visa transformar a forma como os usuários interagem com o GitHub, introduzindo elementos de gamificação que incentivam o uso contínuo e eficiente da plataforma. O sistema será desenvolvido seguindo as melhores práticas de engenharia de software e design centrado no usuário, garantindo uma experiência envolvente e motivadora.

Ao implementar as funcionalidades descritas neste documento, o GitFica tem o potencial de aumentar significativamente o engajamento dos usuários com o GitHub, melhorar a colaboração em equipes de desenvolvimento e proporcionar uma visão clara do progresso individual e coletivo nas atividades de desenvolvimento de software.