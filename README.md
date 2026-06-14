# Cetoacidose diabética — apoio ao plantão

Ferramenta web de apoio à beira-leito para o manejo da **cetoacidose diabética (CAD)** no adulto. Página única, sem dependências, funciona offline.

> ⚠️ **Apoio à conduta — não substitui protocolo institucional nem julgamento clínico.** Conteúdo educacional. Sempre confirme doses e adapte ao seu serviço.

## O que tem

- **Card de beira-leito** — referência rápida (diagnóstico, gravidade, fluido, insulina, potássio, metas, fórmulas) com botão de impressão.
- **Checklist do plantão** — condutas por fase, com o *gate* do potássio embutido: os passos de insulina ficam travados até o K⁺ ser dosado. Progresso salvo no navegador.
- **Algoritmo animado** — as três infusões (fluido / insulina / potássio) correndo em paralelo no tempo, com o gate do K⁺ e o loop horário.
- **Dúvidas & armadilhas** — as situações imperfeitas do plantão (glicemia < 250 e a insulina, bicarbonato, sódio corrigido, K⁺ limítrofe, queda rápida demais, sem bomba, anúria, CAD euglicêmica, transição para SC, EHH).

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `index.html` | A ferramenta web (este site). |
| `cad-folha-controle.tex` | Folha de controle imprimível (A4 paisagem, P&B, frente e verso). |
| `cad-folha-controle.pdf` | PDF compilado da folha de controle. |
| `cad-fluxo-clinico.md` | Documento de referência do fluxo clínico (Mermaid + flashcards). |

## Uso local

Abra o `index.html` direto no navegador, ou sirva a pasta:

```bash
python3 -m http.server 4173
# http://localhost:4173/
```

Para recompilar a folha de controle:

```bash
pdflatex cad-folha-controle.tex
```
