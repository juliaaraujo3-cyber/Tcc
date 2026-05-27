# TCC – Medicina Veterinária – UFLA

Projeto LaTeX formatado no padrão **ABNT NBR 14724:2011** com abnTeX2.

## Estrutura

```
Tcc/
├── main.tex                     # Arquivo principal
├── references.bib               # Referências BibTeX
├── figures/                     # Figuras e imagens
├── pretextual/
│   ├── capa.tex
│   ├── folha-rosto.tex
│   ├── folha-aprovacao.tex
│   ├── dedicatoria.tex
│   ├── agradecimentos.tex
│   ├── epigrafe.tex
│   ├── resumo.tex
│   └── abstract.tex
└── chapters/
    ├── 01-introducao.tex
    ├── 02-revisao-literatura.tex
    ├── 03-material-metodos.tex
    ├── 04-resultados-discussao.tex
    └── 05-conclusao.tex
```

## Como compilar

### Opção 1 – Overleaf (recomendado, sem instalação)
1. Faça o download de todos os arquivos como `.zip`
2. Acesse [overleaf.com](https://www.overleaf.com) → New Project → Upload Project
3. Clique em **Recompile** (usa pdfLaTeX por padrão)

### Opção 2 – Localmente (TeX Live)
```bash
sudo apt install texlive-full
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Preencher o conteúdo

1. Edite `main.tex` e coloque seu nome, título e orientador
2. Preencha `pretextual/resumo.tex` e `pretextual/abstract.tex`
3. Cole o conteúdo de cada capítulo nos arquivos `chapters/*.tex`
4. Adicione suas referências em `references.bib`
5. Coloque figuras na pasta `figures/`

## Citações ABNT

| Tipo | Comando | Resultado |
|------|---------|-----------|
| Indireta | `\cite{autor2020}` | (AUTOR, 2020) |
| Direta com nome | `\citeonline{autor2020}` | Autor (2020) |
| Múltiplas | `\cite{a2020, b2019}` | (A, 2020; B, 2019) |
| Apud | `\apud{fontesecundaria}{fonteprimaria}` | apud |
