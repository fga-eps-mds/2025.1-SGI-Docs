# Django Rest e Next.js

Documenta a realização do Dojo de Docker com o time.

**Data:** 10/05/2025      
**Horário:** 10h        
**Duração:** 50 min  
**Local:** Discord  
**Elaborador:** Jackes

## Estrutura do Dojo

- **Primeira parte:** uma explicação sobre o Docker
- **Segunda parte:** apresentação da estrutura do docker do projeto
- **Terceita parte:** Configuração do Docker
- **Quarta parte:** Subir os ambientes de Frontend e Backend do projeto

## Lista de presença

| Nome                              | Presente (✅/❌) | Justificativa da Ausência               |
|-----------------------------------|-------------------|-----------------------------------------|
| Danilo Domingo                    |     ✅           |                                         |
| Gabi Ribeiro                      |    ❌           |    Motivos Pessoais                                     |
| Jackes Tiago                      |     ✅           |                                         |
| Arthur Gomes Oliveira             |     ✅           |                                         |
| Caio Vilas Boas Miranda           |     ✅           |                                         |
| Carlos Eduardo Figueiredo Coelho  |     ✅           |                      |
| Daniel da Silva Batista           |     ✅           |                                         |
| Guilherme Nascimento Tegnoue      |     ❌           |    Motivos Pessoais                                      |
| Gustavo Augusto Da Silva Sousa    |     ✅           |                                         |
| Janio Lucas Pereira Carrilho      |     ❌           |    Motivos Pessoais                                      |
| João Guilherme Capozzi Gonçalves  |     ❌           |    Motivos Pessoais                                      |
| Joao Guilherme Lima Veras         |     ✅           |                                         |
| Pedro Vieira Antunes              |     ✅           |                                         |

## Link da apresentação
<iframe width="560" height="315" src="https://www.youtube.com/watch?v=9Sq5OriiedI" frameborder="0" allowfullscreen></iframe>

## Slides
<iframe src="https://docs.google.com/presentation/d/1g3pQkr83pHEXh0ItWudiwtnU7QqTZvyHMiYdYUWc2Yo/edit?usp=sharing" width="640" height="480" allow="autoplay"></iframe>

## Lista de comandos básicos
```bash
# Verificar versão instalada
docker --version

# Listar imagens
docker images

# Listar containers em execução
docker ps

# Remover imagens (exemplo: docker rmi nome_da_imagem ou ID)
docker rmi nome_da_imagem

# Remover container (exemplo: docker rm nome_do_container ou ID)
docker rm nome_do_container

# Parar e remover todos os containers
docker stop $(docker ps -q) && docker rm $(docker ps -aq)

# Docker Compose - subir os serviços
docker compose up

# Docker Compose - parar e remover os serviços
docker compose down
```

## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 12/05/2025 | Adiciona relato do dojo   | Jackes Fonseca         | 
