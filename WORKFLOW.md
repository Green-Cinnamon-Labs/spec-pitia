# Como trabalho nesta linha

O método é o mesmo da linha Hefesto ([`spec-hefesto/WORKFLOW.md`](https://github.com/Green-Cinnamon-Labs/spec-hefesto/blob/main/WORKFLOW.md)). Aqui fica só o que muda.

## Papéis

- **Eu escrevo os notebooks, o código e o livro.** O Claude não edita nem commita notebooks (`nucleo/`, `digressoes/`, `matematica/`, `revisando/`), nem `codigo/`, nem `praticas/`.
- **O Claude guia.** Nas práticas, por versão: "o que está assim hoje → mude para → por quê (1 a 3 linhas)", e como conferir. Nas leituras, ajuda a ler o artigo e a checar as fontes.
- O Claude pode escrever e commitar documentação do hub (README, WORKFLOW, `referencias/papers.md`).

## Três tipos de issue

Todas ficam neste hub e no [board](https://github.com/orgs/Green-Cinnamon-Labs/projects/12), com Linha = Pítia. O título começa pelo tipo.

- **`[leitura]`**: um artigo. Seções fixas: o que afirma, em que camada da pilha mexe, o que muda na distância até um problema útil e o que a comunidade respondeu. A issue fecha com um comentário meu, com a minha leitura, e com o artigo registrado em `referencias/papers.md`.
- **`[prática]`**: código que roda, em versões (v0 ingênua até vN), como nas outras linhas. O código fica em `praticas/`.
- **`[hub]`**: arrumação do repositório.

## Livro

LaTeX em [`book/`](book/), uma parte por camada: problema, algoritmo, correção de erros, hardware e mercado. Os fundamentos dos notebooks entram como capítulos da parte de algoritmo. Os notebooks continuam no repositório como o lado executável.

## GitHub Flow

1. Uma branch por issue de prática: `<tipo>/<n>-<resumo>`, por exemplo `feat/4-bell-state`.
2. Um commit por versão, e um comentário na issue por versão.
3. PR em inglês, merge sem squash.
4. Leituras e arrumação podem ir direto na `main`.

## Commits

[Conventional Commits](https://www.conventionalcommits.org/), em inglês, com `Refs #N`.

## Repositórios

Ficam todos lado a lado em `C:\Projetos\gclabs\`, e o workspace é o [`pitia.code-workspace`](pitia.code-workspace). As configurações do editor ficam no workspace, porque a `.vscode/` está no `.gitignore`.

| Pasta | O que é |
| --- | --- |
| `spec-pitia` | este hub: os notebooks, o livro, as issues e este fluxo |

Quando surgir um repositório novo da linha:

1. Clone ao lado dos outros, em `C:\Projetos\gclabs\`.
2. Acrescente a pasta em `folders` no workspace e uma linha nesta tabela.
3. As issues continuam neste hub, com o repositório no título (`[prática][<repo>] ...`), e os commits do repositório novo usam `Refs Green-Cinnamon-Labs/spec-pitia#N`.
