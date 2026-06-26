# Como aplicar a atualização no GitHub Profile README

Este pacote atualiza o profile público `AKA-Nata/AKA-Nata` com:

- README mais visual e direto;
- GitHub Readme Stats;
- resumo técnico atualizado com projetos recentes;
- SVGs animados atualizados;
- descrição segura dos projetos internos, sem hosts, IPs, schemas, tabelas, endpoints privados ou credenciais.

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
git commit -m "Update profile README with current integration projects"
git push
```

## 5. Observação sobre GitHub Readme Stats

Os cards usam a instância pública:

```text
https://github-readme-stats.vercel.app
```

Ela reflete principalmente dados públicos/visíveis do GitHub. Trabalho corporativo em repositórios privados normalmente não aparece nos cards, por isso o README também mantém uma seção textual com resumo seguro dos projetos internos.


## 6. Observação sobre GitHub Readme Stats

O README usa a versão robusta do card de estatísticas:

```text
&hide=commits&hide_rank=true
```

Motivo: a instância pública do `github-readme-stats.vercel.app` pode falhar ao buscar total de commits, especialmente com `include_all_commits=true`, cache, limite da API pública ou dados privados/corporativos que não aparecem no token público.

Se quiser mostrar commits totais no futuro, o caminho mais estável é subir uma instância própria do GitHub Readme Stats com token GitHub configurado.
