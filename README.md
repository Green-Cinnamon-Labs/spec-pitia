# spec-pitia

> A Pítia, sacerdotisa do oráculo de Delfos, dava respostas que só faziam sentido como probabilidades a interpretar.

Linha de pesquisa do [Green Cinnamon Labs](https://github.com/Green-Cinnamon-Labs) sobre computação quântica.

## O que sei hoje

- Quero entender como funcionam os computadores quânticos e as implementações físicas que eles têm hoje.
- Quero acompanhar os breakthroughs e os algoritmos de correção de erros.
- Quero entender os problemas que eles supostamente vão resolver, como descobrir a carteira de investimento mais eficiente.
- Quero acompanhar os artigos no arXiv ([`referencias/`](referencias/)).
- O maior desafio para quem quer aplicar computação quântica a um problema real é saber formalizá-lo: estados, operadores, preparação e medição.

Isto muda conforme eu avanço.

## O eixo da linha

Uma pergunta organiza tudo: **quanto falta para um computador quântico resolver um problema útil, e qual?** Responder é descer uma pilha:

| Camada | Pergunta |
| --- | --- |
| Problema | Que problema real espera por isso, e como ele vira operador? |
| Algoritmo | O que o circuito extrai, e a que custo? |
| Correção de erros | Quantos qubits físicos fazem um qubit lógico? |
| Hardware | Que tecnologia entrega esses qubits, e com que erro? |
| Mercado | Quem vende cada camada, e o que dá para usar hoje? |

Os artigos atravessam todas as camadas: cada um é lido perguntando em que camada mexe e quanto encurta a distância. A medida que acompanha isso é a estimativa de recursos (qubits e tempo por problema) contra o que o hardware entrega.

As issues ficam neste hub e no [board](https://github.com/orgs/Green-Cinnamon-Labs/projects/12) (Linha = Pítia). O jeito de trabalhar está em [`WORKFLOW.md`](WORKFLOW.md).

## Livro

[`book/`](book/), em LaTeX, sobre computação quântica. Abre com os fundamentos, a partir da pergunta de Feynman (o qubit, a mecânica quântica e a álgebra linear), e depois tem uma parte por camada da pilha. A parte de problemas reúne vários deles, e a fatoração é só um.
