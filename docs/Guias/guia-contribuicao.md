# Guia de contribuição

## Como contribuir
- Se você for um colaborador externo, dê um fork no projeto  
- Issues só poderão ser criadas com os templates especificados no repositório  
- A criação de branches deve seguir a política de branches  
- No desenvolvimento usar nossa política de commits  
- Pull requests só serão aceitos se estiverem com o template especificado no repositório  
- **Antes de enviar qualquer contribuição, leia atentamente as diretrizes descritas neste documento e certifique-se de que sua alteração está alinhada com os objetivos do projeto**  
- **Revise o código antes de abrir um Pull Request, garantindo que ele esteja funcionando corretamente e que não quebre funcionalidades existentes**  
- **Inclua testes sempre que possível, principalmente ao adicionar novas funcionalidades**  
- **Descreva claramente no Pull Request o que foi feito, o motivo e como testar**

## Política de Branches

Nossa política segue algumas características do Gitflow. Então separamos nossas branches em:

### `main`

A `main` será nossa branch de produção, ou seja, nela estará a versão estável do projeto.  
Por questões de segurança, ela será bloqueada para commits e push.  
A interação com a `main` ocorrerá através de Pull Requests que virão da branch `devel`.

### `devel`

A `devel` será nossa branch de desenvolvimento, ou seja, vai agrupar o trabalho vindo das branches de features.  
O objetivo é criar uma release que será submetida para a `main`.

### Branches de Features

As branches de features são criadas a partir da `devel`, e servem para o desenvolvimento de funcionalidades presentes nas issues do repositório.  
No final do desenvolvimento, a funcionalidade desenvolvida nessa branch deve ser enviada para a `devel` através de um Pull Request.

**Padrão de nomenclatura**:  
`X_Nome_da_issue`, onde `X` é o número da issue correspondente à funcionalidade.

### Hotfix Branches

Branches do tipo `hotfix` são criadas a partir da `main` e servem para resolver de forma rápida os bugs em produção.

**Padrão de nomenclatura**:  
`hotfix_Nome_do_bug`

---

## Política de Commits

Os commits devem descrever de forma simples e sucinta as modificações feitas.  
Devem ser escritos em **português**.

**Exemplo**:

```bash
git commit -m "Cria nova model"
```

### Commits em Pares

Quando se utiliza a técnica de pair programming, deve-se deixar especificado todos os autores envolvidos no desenvolvimento da funcionalidade.
Para isso, use a tag Co-authored-by do GitHub.

```bash
$ git commit -m "Refactor usability tests.
>
> Co-authored-by: NAME <NAME@EXAMPLE.COM>
> Co-authored-by: ANOTHER-NAME <ANOTHER-NAME@EXAMPLE.COM>"
```

## Políticas de issue
Antes de abrir uma nova issue, siga as boas práticas abaixo:

- **Verifique se a issue já existe**: Pesquise na aba de _issues_ do repositório do projeto **GitFica**. Utilize palavras-chave relevantes e filtros por _labels_ para facilitar a busca.  
- **Consulte os templates disponíveis**: Há modelos específicos para diferentes tipos de contribuição, como: relato de bugs, histórias de usuário e issue genérica.

### Como Abrir uma Issue

Para registrar uma issue no projeto **GitFica**, siga estas etapas:

1. Acesse o repositório de documentação do projeto.  
2. Clique na aba **Issues**.  
3. Selecione **New issue**.  
4. Escolha o _template_ adequado para o seu caso:
   - 🪲 **Bug report** — para relatar falhas ou comportamentos inesperados.
   - 📘 **História de Usuário** — para descrever requisitos funcionais sob a perspectiva do usuário
   - 📝 **Genérica** — para qualquer outro tipo de contribuição que não se encaixe nos templates acima.


5. Preencha **todas as seções** do template com o máximo de clareza e detalhe possível:
   - Um **título direto e informativo**.
   - Uma **descrição clara** do problema, sugestão ou dúvida.
   - Um **passo a passo detalhado** (obrigatório para bugs) para reproduzir o comportamento relatado.
   - Informações sobre o **ambiente de execução**: sistema operacional, versões das ferramentas utilizadas, dependências instaladas, entre outros.

## Dicas Finais

- Seja claro, objetivo e respeitoso com a comunidade e com os mantenedores do projeto.  
- Sempre que possível, **anexe evidências** que ajudem na análise, como capturas de tela, trechos de código ou logs.  
- Caso a issue seja resolvida e ainda esteja aberta, **considere encerrá-la manualmente** se aplicável.  
- Lembre-se: abrir uma issue vai além de apontar um problema — é uma forma de **colaborar ativamente com a evolução do projeto**.


## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 15/05/2025 | Adiciona guia de contribuição   | Jackes Fonseca         |