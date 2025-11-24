---

# 📘 Comandos Git Essenciais

Lista prática dos comandos mais úteis para trabalhar com Git e GitHub no dia a dia.

---

## 🔹 Inicialização e Status

```bash
git init
git status
```

---

## 🔹 Adicionar e Committar

```bash
git add .
git add arquivo.ext
git commit -m "mensagem"
git commit --amend        # Edita o último commit
git log                   # Mostra histórico de commits
```

---

## 🔹 Branches

```bash
git branch                # Lista branches
git branch -M main        # Renomeia branch atual para main
git branch nova-branch    # Cria nova branch
git checkout nova-branch  # Troca para outra branch
git checkout -b nova      # Cria e já troca
git merge nome-da-branch  # Faz merge
```

---

## 🔹 Remotes

```bash
git remote -v
git remote add origin https://github.com/usuario/repositorio.git
git remote add publico https://github.com/usuario/repositorio-publico.git
git remote set-url origin https://github.com/usuario/novo-repo.git
git remote remove origin
git remote rm origin
```

---

## 🔹 Push e Pull

```bash
git push -u origin main
git push origin main
git push --force origin main
git pull
git pull origin main
```

---

## 🔹 Reset / Undo

```bash
git reset --soft HEAD~1       # Reverte commit mantendo alterações
git reset --hard HEAD~1       # Reverte commit apagando alterações
git restore arquivo.ext       # Restaura arquivo modificado
git checkout -- arquivo.ext   # Forma antiga do restore
```

---

## 🔹 Clonar e Duplicar Repositórios

```bash
git clone https://github.com/user/repo.git
git clone --bare repo.git     # Para duplicar repositórios
```

---

## 🔹 Limpar Histórico (útil para repos públicos)

```bash
rm -rf .git                   # Remove o histórico
git init                      # Inicia novo repositório do zero
```

---
