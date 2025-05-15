# Política de Branches

Nossa política segue algumas características do Gitflow. Então separamos nossas branches em:

## `main`

A `main` será nossa branch de produção, ou seja, nela estará a versão estável do projeto.  
Por questões de segurança, ela será bloqueada para commits e push.  
A interação com a `main` ocorrerá através de Pull Requests que virão da branch `devel`.

## `devel`

A `devel` será nossa branch de desenvolvimento, ou seja, vai agrupar o trabalho vindo das branches de features.  
O objetivo é criar uma release que será submetida para a `main`.

## Branches de Features

As branches de features são criadas a partir da `devel`, e servem para o desenvolvimento de funcionalidades presentes nas issues do repositório.  
No final do desenvolvimento, a funcionalidade desenvolvida nessa branch deve ser enviada para a `devel` através de um Pull Request.

**Padrão de nomenclatura**:  
`X_Nome_da_issue`, onde `X` é o número da issue correspondente à funcionalidade.

## Hotfix Branches

Branches do tipo `hotfix` são criadas a partir da `main` e servem para resolver de forma rápida os bugs em produção.

**Padrão de nomenclatura**:  
`hotfix_Nome_do_bug`

## Histórico de Versões

| Versão | Data       | Modificação                | Autor(es)         |
|--------|------------|----------------------------|-------------------|
|   1.0  | 15/05/2025 | Adiciona política de branch   | Jackes Fonseca         |