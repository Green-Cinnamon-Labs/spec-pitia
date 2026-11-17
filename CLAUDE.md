# Linha Pítia

Leia `WORKFLOW.md` antes de qualquer coisa. O eixo da linha está no `README.md`: quanto falta para um computador quântico resolver um problema útil, e qual.

- Nunca edite, crie ou commite notebooks (`nucleo/`, `digressoes/`, `matematica/`, `revisando/`), nem arquivos em `codigo/` ou `praticas/`. Quem escreve é o usuário. Leia o que for preciso para guiar e revisar.
- Guie as práticas por versão: "o que está assim hoje → mude para → por quê (1 a 3 linhas)", e depois como conferir. Sem teoria na sessão.
- Todo conceito novo vem com a genealogia: quando surgiu, que problema o forçou a existir, o que ele corrige da solução anterior. Nunca regras soltas.
- O livro (`book/`) é ditado pelo usuário. Não escreva nada nele sem um pedido explícito.
- Números de hardware, de correção de erros e de estimativa de recursos mudam rápido. Confira na fonte primária (arXiv, artigo publicado, documentação do fabricante) antes de afirmar, e diga a data do dado.

## Um chat por issue

O usuário abre um chat para cada issue e um só para o livro. Ao começar o chat de uma issue:

1. Leia a issue e os comentários (`gh issue view <n> -R Green-Cinnamon-Labs/spec-pitia --comments`) e as issues citadas em "Depende de" ou "Relacionadas".
2. `[leitura]`: baixe o resumo do arXiv, situe o artigo na pilha e acompanhe a leitura seção por seção. Procure as respostas da comunidade (comentários, artigos que o contestam ou reproduzem) antes de concluir.
3. `[prática]`: descubra em que versão o usuário está (checklist, comentários de versão, branch e commits) e comece pela próxima versão não marcada.
4. Se faltar alguma dependência, avise antes de começar.

## Livro

- LaTeX em `book/`. MiKTeX e latexmk estão instalados. Depois de cada mudança, recompile o PDF e atualize o índice em `book/README.md`.
- História real: pessoas, datas, o problema que forçou cada ideia. Nada de histórias inventadas.
- Nunca o código literal do projeto (notebooks, práticas, versões de issue). O livro é uma conversa paralela sobre por que as coisas são como são.
- Fatos exatos, opiniões categóricas. A história tem que estar certa. Na análise, diga o que soa, sem medo e sem ressalvas: "isso é marketing", "isso é um erro". O livro não é científico; prefira pecar pela imprecisão a deixar o leitor sem posição.
- Nada de tom irônico nem de frases de efeito com cara de texto de IA: "That isn't X. It's Y.", aforismos curtos em sequência, fechamentos de impacto. Diga a coisa direto, numa frase simples.
- Tom leve. Todo exemplo de código que entrar no livro tem que ser rodado antes.
- Arquivos `.tex` se editam com o Edit, não com sed ou printf, por causa das barras invertidas.
- Seja objetivo: sem recaps e sem listas de próximos passos.
- Fechamento só quando o usuário disser "close-out": comentário na issue, texto do PR e release.
