# Branches e Merge

## O que são branches?

Branches (ou ramificações) são como linhas paralelas de desenvolvimento dentro de um projeto Git.

Elas permitem que várias pessoas ou equipes trabalhem em diferentes funcionalidades ou correções **ao mesmo tempo**, sem afetar o código principal (geralmente a branch `main`).

Quando o desenvolvimento na branch é concluído, as alterações podem ser **mescladas** de volta à `main`.

---

## Como criar uma branch?

Para criar uma nova branch e já alternar para ela, usamos:

```bash
git checkout -b nome-da-branch
