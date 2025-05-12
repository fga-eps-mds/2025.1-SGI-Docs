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

<video src="https://www.youtube.com/watch?v=9Sq5OriiedI" width="320" height="240" controls></video>


## Slides
<div style="position: relative; width: 100%; height: 0; padding-top: 56.2500%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https://www.canva.com/design/DAGnQE6qkYg/gnUrSWK4PfnjEdX2UP-z_g/view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAGnQE6qkYg&#x2F;gnUrSWK4PfnjEdX2UP-z_g&#x2F;view?utm_content=DAGnQE6qkYg&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener">Dojo Docker.pptx</a> by Jackes da Fonseca

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
