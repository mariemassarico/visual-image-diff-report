# 🖼️ Visual Image Diff Report

Este repositório contém um script para gerar relatórios visuais de diferença entre imagens. Ele é útil para detectar mudanças visuais em interfaces, imagens processadas ou capturas automatizadas, auxiliando testes visuais e revisões gráficas.

---

## ✅ Pré-requisitos

### macOS

- Instale o [ImageMagick](https://imagemagick.org):
```bash
brew install imagemagick
```

### Windows

Use [WSL](https://learn.microsoft.com/pt-br/windows/wsl/install) ou [Git Bash](https://gitforwindows.org/) e instale o ImageMagick:

- Usando Chocolatey:
```powershell
choco install imagemagick
```

- Ou usando Winget:
```powershell
winget install ImageMagick
```

---

## ▶️ Como Rodar

### macOS / Linux

```bash
chmod +x cypressInstallMac.sh
./cypressInstallMac.sh
```

### Windows (via Git Bash ou WSL)

```bash
chmod +x cypressInstallWindows.sh
./cypressInstallWindows.sh NomeDaPasta Autor VersaoDoCypress(opicional)
```
---

## 📜 Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

---

## ✨ Contribuições

Sinta-se à vontade para abrir issues ou PRs com melhorias, correções ou sugestões!


---

## ▶️ Como Rodar a validação das telas?

Após instalação, instale as dependências
```bash
npm install
```

e escrita dos testes no cypress, na tela que você deseja validar vai colocar o comando:

```bash
cy.compareSnapshot(nomeDaTela)
```

após rodar os testes, seja pelo modo interativo ou pelo modo headless, você vai gerar os relatórios
```bash
npx cypress-image-diff-html-report generate
cypress-image-diff-html-report start --autoOpen
```

Isso levara você a uma tela de validação das telas em questão
