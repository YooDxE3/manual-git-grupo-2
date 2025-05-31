##Guilherme Ananias Calixto Ribeiro    14652 

# 🔀 Manual de Pull Request no Git

Este guia explica como criar um Pull Request (PR) no GitHub, facilitando a colaboração e revisão de código em projetos.

---

## 1. ❓ O que é um Pull Request?

Um Pull Request (PR) é uma solicitação para mesclar suas alterações em um repositório principal. Ele permite revisão de código, discussões e colaboração antes da integração.

---

## 2. 🚀 Passos para criar um Pull Request

### 2.1. Faça um Fork (se necessário)
Se não tiver permissão no repositório principal:
1. Clique em **Fork** no GitHub para criar uma cópia do repositório na sua conta.

### 2.2. Clone o repositório
```bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
cd NOME_DO_REPOSITORIO
```

### 2.3. Crie uma nova branch
```bash
git checkout -b nome-da-sua-branch
```

### 2.4. Faça suas alterações
Edite, adicione ou remova arquivos conforme necessário.

### 2.5. Adicione e faça commit das alterações
```bash
git add .
git commit -m "Descrição clara das alterações"
```

### 2.6. Envie sua branch para o repositório remoto
```bash
git push origin nome-da-sua-branch
```

### 2.7. Crie o Pull Request
1. Acesse o repositório no GitHub.
2. Clique em **Compare & pull request** ou **New pull request**.
3. Escolha a branch de origem (a sua) e a branch de destino (geralmente `main` ou `develop`).
4. Preencha o título e a descrição do PR.
5. Clique em **Create pull request**.

---

## 3. 💡 Boas práticas

- Faça commits pequenos e com mensagens claras.
- Descreva bem o que foi alterado no PR.
- Revise o código antes de solicitar o PR.
- Responda comentários dos revisores.

---

## 4. 🔄 Fluxo de revisão

1. Aguarde revisão dos responsáveis pelo repositório.
2. Faça ajustes se solicitado.
3. Após aprovação, o PR será mesclado.

---

## 5. 📚 Referências

- [Documentação oficial do GitHub Pull Requests](https://docs.github.com/pt/pull-requests)
