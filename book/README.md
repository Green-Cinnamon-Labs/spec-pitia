# Livro

O livro desta linha: o meu estudo, escrito conforme eu avanço. Uma parte por camada da pilha (problema, algoritmo, correção de erros, hardware, mercado); dentro de cada parte, os capítulos entram na ordem em que aparecem.

Escrito em inglês. Compilar: `latexmk -pdf main.tex` nesta pasta (gera `main.pdf`).

## Padrão visual

Definido em [pitia.sty](pitia.sty), o mesmo padrão do livro do Hefesto.

- Caixa âmbar, `\begin{history}{ano · lugar}`: uma história, com quem, quando e o que forçou a ideia.
- Caixa azul, `\begin{concept}{nome}`: um conceito-chave, com o que é, o que corrige e o que custa.
- Código em `\begin{code}` (Python por padrão) e a saída de um comando em `\begin{terminal}`. Todo exemplo foi rodado antes de entrar, e a saída é a que ele imprimiu.
- Notação de Dirac com o pacote `braket`: `\ket{0}`, `\bra{\psi}`, `\braket{\phi|\psi}`.
- Diagramas em TikZ, com os estilos `hf/*` do `.sty`.

## Índice

Ainda sem capítulos.
