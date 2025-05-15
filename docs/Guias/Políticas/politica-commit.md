# Política de Commits

Os commits devem descrever de forma simples e sucinta as modificações feitas.  
Devem ser escritos em **português**.

**Exemplo**:

```bash
git commit -m "Cria nova model"
```

## Commits em Pares

Quando se utiliza a técnica de pair programming, deve-se deixar especificado todos os autores envolvidos no desenvolvimento da funcionalidade.
Para isso, use a tag Co-authored-by do GitHub.

```bash
$ git commit -m "Refactor usability tests.
>
> Co-authored-by: NAME <NAME@EXAMPLE.COM>
> Co-authored-by: ANOTHER-NAME <ANOTHER-NAME@EXAMPLE.COM>"
```
## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 15/05/2025 | Adiciona politica de commit   | Jackes Fonseca         |