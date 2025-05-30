## Murilo Sousa Joaquim-14541

# 📥 Instalação e Configurações do Git

Este guia explica como instalar o Git no seu sistema e como realizar as configurações iniciais necessárias para utilizá-lo.

---

## 1. 🔧 Instalação do Git

### Windows
1. Acesse o site oficial: [https://git-scm.com/](https://git-scm.com/)
2. Baixe o instalador do Git para Windows.
3. Execute o instalador e siga as instruções (as configurações padrão são suficientes).
4. Após a instalação, abra o **Git Bash** para utilizar o Git via terminal.

### macOS
Se você tem o Homebrew instalado, basta rodar:
```bash
brew install git

## Linux (Ubuntu/Debian)
  No terminal:
$ sudo apt update
$ sudo apt install git

----

## 2. Configurações Iniciais

## Após a instalação, é necessário configurar seu nome de usuário e e-mail:
$ git config --global user.name "Seu Nome"
$ git config --global user.email "seuemail@exemplo.com"
## Essas informações aparecem em todos os commits feitos por você.

-----

## 3. Verificando as Configurações

## Para verificar se as configurações foram salvas corretamente:
$ git config --list

----

## 4. Outras Configurações Ùteis

## Definir o editor de texto padrão (exemplo: VS Code)
$ git config --global core.editor "code --wait"

## Ativar cores no terminal
$ git config --global color.ui auto

-----

## 5. Verificando se o Git está funcionando

## Execute o comando abaixo no terminal:
$ git --version

## Se tudo estiver certo, o terminal mostrará a versão do Git, por exemplo:
$ git version 2.43.0

-----

## 6. Exemplo Prático

# Criando uma pasta e iniciando um repositório Git
mkdir meu-projeto
cd meu-projeto
git init

# Criando um arquivo e fazendo o primeiro commit
echo "# Meu Projeto" > README.md
git add README.md
git commit -m "primeiro commit"

-----

## Após seguir todos estes passos, você está pronto para começar a usar o Git
## e colaborar com repositórios no GitHub!

