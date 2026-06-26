# Como aplicar a atualização no GitHub Profile README

Este pacote atualiza o profile público `AKA-Nata/AKA-Nata` com:

- README mais visual e direto;
- resumo técnico atualizado com projetos recentes;
- SVGs animados atualizados;
- descrição segura dos projetos internos, sem hosts, IPs, schemas, tabelas, endpoints privados ou credenciais;
- remoção dos cards públicos de GitHub Stats, já que eles não representam bem commits/pushes privados ou corporativos.

## 1. Clone o repositório de profile

```powershell
git clone https://github.com/AKA-Nata/AKA-Nata.git
cd AKA-Nata
```

Se você já tem o repositório local:

```powershell
cd C:\caminho\para\AKA-Nata
git pull
```

## 2. Copie os arquivos deste pacote para a raiz do repositório

Copie/substitua:

```text
README.md
README_SNIPPET.md
terminal.svg
typing.svg
pipeline.svg
session.cast
.gitignore
PROFILE_CHANGELOG.md
```

## 3. Valide antes do commit

```powershell
git status --short
```

O esperado é aparecerem apenas arquivos públicos do profile. Não publique:

- `.env`;
- zips brutos;
- logs;
- prints com dados reais;
- arquivos de credenciais;
- documentos internos;
- nomes de tabelas/schemas sensíveis;
- hosts, IPs ou endpoints internos.

## 4. Commit e push

```powershell
git add README.md README_SNIPPET.md terminal.svg typing.svg pipeline.svg session.cast .gitignore PROFILE_CHANGELOG.md
git commit -m "Remove GitHub stats cards from profile README"
git push
```

## 5. Observação sobre dados privados

O README agora prioriza uma apresentação textual/arquitetural do seu escopo de atuação. Isso evita que cards públicos mostrem uma visão incompleta, já que commits, pushes e repositórios privados/corporativos normalmente não entram nas estatísticas públicas do GitHub.
