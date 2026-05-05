# Como subir no GitHub

## 0. Atenção ao arquivo de dados profissionais

O arquivo `dados_profissionais_nata_rafael_barbosa.md` é uma base local de referência para LinkedIn, currículo, GitHub e portfólio.

Não publique esse arquivo bruto no repositório público do perfil. Ele contém informações mais detalhadas do que o necessário para um README público. O `README.md` já foi montado com uma versão filtrada e segura dessas informações.

Este pacote também inclui um `.gitignore` para ajudar a evitar upload acidental desse arquivo.

## 1. Criar o repositório de perfil

No GitHub, crie um repositório público com o mesmo nome do seu usuário:

```text
AKA-Nata/AKA-Nata
```

Esse nome é obrigatório para o GitHub exibir o `README.md` diretamente no seu perfil.

## 2. Subir os arquivos pelo VS Code / terminal

```powershell
mkdir AKA-Nata
cd AKA-Nata

git init

git remote add origin https://github.com/AKA-Nata/AKA-Nata.git
```

Copie estes arquivos para dentro da pasta:

```text
README.md
terminal.svg
session.cast
.gitignore
```

Depois rode:

```powershell
git add README.md terminal.svg session.cast .gitignore
git commit -m "Create animated GitHub profile README"
git branch -M main
git push -u origin main
```

## 3. Caso o repositório já exista

Clone primeiro:

```powershell
git clone https://github.com/AKA-Nata/AKA-Nata.git
cd AKA-Nata
```

Copie os arquivos para dentro da pasta clonada e rode:

```powershell
git add README.md terminal.svg session.cast .gitignore
git commit -m "Update profile README with animated terminal"
git push
```

## 4. Como usar o session.cast com TermSVG

Este pacote já inclui um `terminal.svg` pronto. Mesmo assim, se quiser gerar pelo TermSVG a partir do `.cast`:

```powershell
termsvg export .\session.cast --output .\terminal.svg
```

Depois faça commit do SVG gerado:

```powershell
git add terminal.svg session.cast
git commit -m "Generate terminal animation"
git push
```

## 5. Observação sobre projetos internos

Os projetos internos foram descritos apenas em nível de propósito, tecnologias e impacto. Evite publicar:

- IPs;
- hosts internos;
- caminhos de rede;
- nomes reais de tabelas internas;
- usuários de execução;
- endpoints privados;
- regras sensíveis de negócio;
- prints com dados reais;
- credenciais, tokens ou arquivos `.env`.

Use `git status --short` antes do commit para confirmar que apenas arquivos públicos entraram no versionamento.
