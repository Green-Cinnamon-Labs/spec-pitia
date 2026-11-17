# spec-pitia

> A Pítia, sacerdotisa do oráculo de Delfos, dava respostas que só faziam sentido como probabilidades a interpretar.

Linha de pesquisa do [Green Cinnamon Labs](https://github.com/Green-Cinnamon-Labs) sobre computação quântica.

## O que sei hoje

- Quero entender como funcionam os computadores quânticos e as implementações físicas que eles têm hoje.
- Quero acompanhar os breakthroughs e os algoritmos de correção de erros.
- Quero entender os problemas que eles supostamente vão resolver, como descobrir a carteira de investimento mais eficiente.
- Quero acompanhar os artigos no arXiv ([`referencias/`](referencias/)).
- Nada aqui é fixo: um tema novo entra no livro quando aparecer, na ordem que fizer sentido.

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

O livro está em [`book/`](book/), em LaTeX, com uma parte por camada. Os notebooks abaixo são o lado executável: os fundamentos entram no livro como capítulos, e os notebooks ficam como o lugar onde as contas rodam.

---

## O caderno: Survey on Quantum Computing

Caderno de pesquisa reproduzível sobre computação quântica. O objetivo dele é explorar uma tese:

<div style="border-left: 2px solid #16a34a; padding: 0.5em 1em 0.5em 1.1em; margin: 0.8em 0 1.2em 0; background: rgba(22, 163, 74, 0.05); border-radius: 0 3px 3px 0;">
  <span style="font-size: 0.65em; font-weight: 700; letter-spacing: 0.13em; text-transform: uppercase; color: #16a34a;">TESE PRINCIPAL</span><br>
  <span style="font-size: 0.88em; line-height: 1.65;">O principal desafio para engenheiros que visam aplicar computação quântica em problemas do cotidiano é desenvolver a intuição de como formalizar um problema real matemáticamente.</span>
</div>

Um QPU não é uma CPU mais rápida. É uma unidade especializada que opera sobre estados quânticos por meio de transformações restritas. O gargalo prático, aqui, é saber formular o problema na linguagem correta: operadores, estados, unitários, observáveis, espectro, preparação, medição.

## Como é a minha abordagem?

Eu sempre faço o notebook ter uma pergunta central que é imediatamente respondida com uma afirmação que o leitor, no início da leitura, não entende. Essa afirmação guia a estruturação do notebook em questão. O objetivo é sempre explorar a afirmação que responde a pergunta do notebook. No final, exponho o que você entendeu — como uma espécie de resumo — e o que aquele notebook não te explicou — para que você perceba que alguma coisa realmente foi omitida de você.

Eu decidi seguir uma abordagem repetitiva. A cada notebook do núcleo, eu praticamente repito as mesmas ideias com cada vez mais complexidade associada. Geralmente, eu vou usar exemplos básicos e ilustrativos para explorar ideias imporatantes e depois vou usar esses mesmos exemplos para formalizar um pouco da matemática, sempre em uma crescente de complexidade.

Vou repetir e relembrar conceitos à exaustão. Uma mesma ideia será repetida dezenas de vezes ao longo dos vários núcleos. Vou usar esquemas visuais feitos com bibliotecas padrão do Python e em um estágio mais avançado, vamos usar `qiskit`. 

A melhor forma de expor como isso está sendo usado sem acomodar demais o leitor é introduzido ele aos problemas reais. É por isso que eu vou explicar usando os artigos reais que firmaram milestones dentro da computação quântica. Meu objetivo é expor o leitor à cronologia dos fatos.

Por fim, eu paralelizo com notebooks especializados em temas específicos. Achei interessante separar em dois grandes blocos: `digressões` e `matemática`. As digressões versam sobre os mesmos assuntos que você encontrará nos notebooks do núcleo. Já a matemática é focada em dar musculatura na intuição matemática e física. 

Por fim, eu considero fundamental entender a etimologia das palavras que são

---

## Como os notebooks são organizados

Os notebooks do **núcleo** partem de uma **pergunta explícita** no título. O bloco de abertura traz **etimologias** dos termos-chave — não como definição, mas como contexto lateral. Em seguida, uma **afirmação introdutória** responde à pergunta diretamente, em uma ou duas frases, às vezes acompanhada de uma fórmula.

O restante do notebook elabora essa afirmação. Termos considerados centrais aparecem destacados em `backtick`. Conexões com outros notebooks aparecem como links de digressão (`↳`) ou de matemática. Ao final, sempre: **"O que este notebook te respondeu"** e **"O que este notebook não respondeu"**.

Os notebooks de **digressão** são desvios curtos e instrumentais: definição mínima → por que importa aqui → exemplo pequeno. Podem ser lidos fora de ordem.

Os notebooks de **matemática** não partem de uma pergunta — eles consolidam um conceito de ponta a ponta, com vínculo explícito ao projeto na última seção.

---

## O que este repositório é

- Caderno de pesquisa reproduzível
- Construído com ordem cronológica de entendimento: cada notebook dá ao leitor a definição útil do conceito antes de usá-lo
- Honesto sobre o que foi e o que não foi aprendido
- Sem dependência de hardware real — apenas simulador

## O que não é

- Não é um curso introdutório genérico
- Não é uma coleção de demos de SDK
- Não é uma promessa de vantagem quântica prática

---

## Trilha Núcleo

Ordem cronológica de entendimento. Cada notebook parte de uma pergunta explícita. As perguntas planejadas estão em [QUESTIONS.md](QUESTIONS.md).

| Código | Pergunta | Status |
|---|---|---|
| [N-00](nucleo/N-00.ipynb) | Por que é possível computar com um qubit? | rascunho |
| [N-01](nucleo/N-01.ipynb) | O que uma operação unitária faz ao estado? | rascunho |
| [N-02](nucleo/N-02.ipynb) | Como eu codifico meu problema usando qubits? | rascunho (conflito de merge a resolver) |
| [N-03](nucleo/N-03.ipynb) | Como eu posso medir o resultado? | esqueleto |

---

## Digressões

Desvios instrumentais curtos. Podem ser lidos fora de ordem.

| Código | Título | Status |
|---|---|---|
| [D-00](digressoes/D-00.ipynb) | O que é um qubit? | rascunho |
| [D-01](digressoes/D-01.ipynb) | A Máquina de Turing | rascunho |
| [D-02](digressoes/D-02.ipynb) | Criptografia e Logaritmos | esqueleto |
| [D-06](digressoes/D-06.ipynb) | O Princípio da Incerteza de Heisenberg | rascunho |
| [D-07](digressoes/D-07.ipynb) | A História da Computação Quântica | rascunho |
| [D-08](digressoes/D-08.ipynb) | Arquiteturas Físicas do Qubit | rascunho |
| [D-09](digressoes/D-09.ipynb) | Correção de Erros em Algoritmos Quânticos | esqueleto |

---

## Matemática

Exploração matemática com vínculo explícito ao projeto. Última seção obrigatória: **"Por que isso importa para algoritmos quânticos?"**

| Código | Título | Status |
|---|---|---|
| [M-00](matematica/M-00.ipynb) | Vetores, Espaços e o Espaço de Hilbert | rascunho |
| [M-01](matematica/M-01.ipynb) | Mecânica Clássica: de Newton a Hamilton | rascunho |
| [M-02](matematica/M-02.ipynb) | Mecânica Quântica: de Planck a Dirac | rascunho |
| [M-04](matematica/M-04.ipynb) | A Transformada de Fourier: da decomposição espectral à QFT | rascunho |
| [M-05](matematica/M-05.ipynb) | Álgebra Linear: das Equações aos Tensores | rascunho |

A pasta [`revisando/`](revisando/) guarda um plano anterior, em inglês, ainda sem destino decidido.

---

## Convenções de status

| Status | Significado |
|---|---|
| `esqueleto` | Arquivo criado, estrutura definida, sem conteúdo real |
| `rascunho` | Conteúdo escrito, não revisado |
| `revisado` | Conteúdo revisado e pergunta verificada como respondida |
| `fechado` | Pergunta marcada como respondida em QUESTIONS.md |

---

## Ambiente

```bash
poetry install
poetry run jupyter lab
```

## Progresso

Ver [ROADMAP.md](ROADMAP.md).
