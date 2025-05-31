
# Branches e Merge

## O que são branches?

Branches (ou ramificações) são linhas paralelas de desenvolvimento dentro de um repositório Git. Imagine o projeto como uma árvore: o tronco principal é a branch `main` (ou `master`), e as branches são ramos que crescem a partir desse tronco.

Elas permitem que você trabalhe em funcionalidades, correções de bugs ou experimentos separadamente do código principal. Assim, o desenvolvimento pode ser feito simultaneamente sem interferir no código estável.

Quando a nova funcionalidade ou correção está pronta e testada, você pode integrar (fazer merge) essa branch de volta à branch principal.

---

## Criar, mudar e deletar branches

### Criar e mudar para uma branch nova

```bash
git checkout -b nome-da-branch
```

- Cria a branch e já muda para ela.

Exemplo:

```bash
git checkout -b feature-login
```

---

### Mudar para uma branch existente

```bash
git checkout nome-da-branch
```

Exemplo:

```bash
git checkout main
```

---

### Listar branches locais

```bash
git branch
```

A branch atual será indicada com um `*`.

---

### Listar branches remotas

```bash
git branch -r
```

---

### Deletar uma branch local

```bash
git branch -d nome-da-branch
```

O Git impede deletar uma branch que ainda não foi mesclada para evitar perda de trabalho. Para forçar a exclusão:

```bash
git branch -D nome-da-branch
```

---

### Deletar uma branch remota

```bash
git push origin --delete nome-da-branch
```

---

## Trabalhando com branches remotas

Para criar uma branch local rastreando uma branch remota:

```bash
git checkout -b nome-da-branch origin/nome-da-branch
```

---

## `git merge` e como lidar com conflitos

### Passos para fazer merge

1. Mude para a branch que vai receber as mudanças:

```bash
git checkout main
```

2. Faça o merge da outra branch:

```bash
git merge nome-da-branch
```

---

### Tipos de merge

- **Fast-forward:** Quando a branch de destino não teve novos commits desde que a branch foi criada, o Git simplesmente avança o ponteiro da branch de destino para o commit da branch mesclada.

- **Merge com commit:** Quando há divergências, o Git cria um commit de merge que junta as histórias das duas branches.

---

### Conflitos de merge

Quando as mesmas linhas de código foram modificadas em ambas as branches, o Git não consegue decidir automaticamente e cria um conflito.

Você verá algo assim no arquivo conflitado:

```plaintext
<<<<<<< HEAD
Conteúdo na branch atual (main)
=======
Conteúdo na branch mesclada (feature-login)
>>>>>>> feature-login
```

---

### Resolvendo conflitos

1. Edite o arquivo para escolher ou combinar o conteúdo desejado.

2. Salve o arquivo.

3. Adicione o arquivo resolvido para o stage:

```bash
git add nome-do-arquivo
```

4. Finalize o merge com um commit:

```bash
git commit
```

O Git automaticamente abre o editor para você escrever a mensagem de commit do merge.

---

## Demonstração passo a passo

Suponha que você tem uma branch `main` e vai criar uma branch para desenvolver uma nova funcionalidade chamada `nova-funcionalidade`:

```bash
# Criar e mudar para a branch nova
git checkout -b nova-funcionalidade

# Fazer alterações nos arquivos
# (editar os arquivos do projeto)

# Adicionar arquivos modificados
git add .

# Criar commit com mensagem
git commit -m "Implementa nova funcionalidade"

# Voltar para a branch principal
git checkout main

# Trazer as alterações da nova branch para a main
git merge nova-funcionalidade

# Caso o merge tenha sido bem-sucedido, pode deletar a branch
git branch -d nova-funcionalidade
```

---

## Boas práticas para usar branches e merge

- **Use nomes claros para branches:** Exemplo: `feature/login`, `bugfix/erro-tela`, `hotfix/seguranca`.

- **Faça commits pequenos e significativos:** Isso facilita a revisão e o merge.

- **Mantenha sua branch atualizada:** Antes de fazer o merge, atualize sua branch com as mudanças da branch principal.

```bash
git checkout sua-branch
git fetch origin
git rebase origin/main
```

- **Evite longos períodos trabalhando em uma branch isolada:** Isso diminui a chance de conflitos complexos.

- **Revise o código antes do merge:** Use pull requests para revisão por colegas, se possível.

---

## Extras: Usando `git rebase` (Opcional)

O `git rebase` serve para “reaplicar” seus commits em cima da última versão da branch principal, deixando o histórico linear e mais limpo.

Exemplo para atualizar sua branch com as últimas mudanças da `main`:

```bash
git checkout sua-branch
git fetch origin
git rebase origin/main
```

⚠️ Atenção: Nunca faça rebase em branches compartilhadas com outras pessoas, pois isso pode complicar o histórico.

---

## Resumo dos comandos principais

| Comando                           | Descrição                            |
|----------------------------------|------------------------------------|
| `git checkout -b nome-da-branch` | Criar e mudar para nova branch      |
| `git checkout nome-da-branch`     | Mudar para branch existente         |
| `git branch`                      | Listar branches locais              |
| `git branch -d nome-da-branch`    | Deletar branch local (mesclada)     |
| `git branch -D nome-da-branch`    | Forçar deletar branch local          |
| `git merge nome-da-branch`        | Mesclar branch na branch atual       |
| `git push origin --delete nome-da-branch` | Deletar branch remota            |
| `git rebase origin/main`          | Reaplicar commits da sua branch em cima da main |

---