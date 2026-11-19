# Capítulo 13: referencial (Majorana 2)

Dados conferidos até 19/11/2026. Marcação: **[conferido]** = li a fonte nesta sessão (página do arXiv, blog, DARPA, imprensa); **[memória]** = sei de cor, conferir quando você baixar o PDF.

Transcrição limpa do vídeo, com tempo: [cap13-majorana-2-transcricao.txt](cap13-majorana-2-transcricao.txt).

## 1. O vídeo

Microsoft, *Majorana 2 Explained: The road to 1000x improvement*. Canal oficial da Microsoft, publicado em 16/11/2026, 8:08 min, legenda manual em inglês. **[conferido]**

O anúncio do Majorana 2 não é de novembro: foi em **2/6/2026**, na Build, com blog do Chetan Nayak e o preprint arXiv:2606.03884 no mesmo dia. O vídeo é uma peça de divulgação cinco meses depois, quando as contestações já tinham saído na Nature. Isso pesa na leitura: ele responde à crítica (5:40) sem citá-la.

### O que o vídeo afirma, e o que a fonte diz

| Tempo | O vídeo diz | O que a fonte diz |
| --- | --- | --- |
| 0:42 | "a thousand x improvement in the stability of our quantum computer" | É o tempo de vida da **paridade Z** de um tetron: τ_Z = 22 ± 1 s no InAs–Pb, contra 1 a 12 ms nos dispositivos de alumínio (2606.03884; blog). **[conferido]** |
| 1:09–1:20 | alumínio trocado por chumbo, antimônio no semicondutor | Pb no lugar de Al; semicondutor InAs + InAsSb sobre substrato de GaSb (The Quantum Insider). Gap de ~30 µeV para ~70 µeV. **[conferido]** |
| 1:37–1:55 | "one error every thousand operations" → "tens of millions of operations before an error" | Confunde o tempo de vida de **um** observável (Z) com a taxa de erro do qubit. Um qubit precisa de X e Z. No dispositivo de 2025, τ_X = 14,5 ± 0,3 µs e τ_Z = 12,4 ± 0,4 ms, com erro de atribuição de 16% em X e 0,5% em Z (2507.08795). O artigo do Majorana 2 não reporta X. **[conferido]** |
| 2:12–2:28 | "multiples of two to three" no material levam a 1000x, porque a dependência é exponencial | Conta na seção 3. O artigo precisa ser lido para ver qual dependência eles usam. |
| 3:16–3:40 | Quantum Development Kit e Quantum Resource Estimator | Ferramenta real e útil; liga com a prática #3 (gráfico de "quanto falta"). |
| 4:25–5:07 | quântico põe "the exact, ground-truth answer" na IA; o Copilot vai "create materials and molecules" | Marketing. Liga com a Parte II (que problemas têm custo conhecido) e com Babbush (2021) no cap. 3. |
| 5:28 | supercondutores à temperatura ambiente, levitação magnética | Marketing: não há estimativa de recursos para isso. |
| 5:40–6:13 | ceticismo é bem-vindo; "there's many things that are proprietary, that we can't share all the details" | A própria empresa admite que não abre tudo. Os erros de código achados pelo Legg só apareceram porque o código foi aberto. |
| 6:38–6:47 | 2029 para "solve some problems that haven't been solved before"; Majorana 3, 4 e 5 | Blog: "cut our timeline in half... by 2029". DARPA: Microsoft está no Stage C do QBI desde o US2QC (página da DARPA de 7/10/2026). Stage C é verificação independente do projeto, não uma máquina entregue. A meta do QBI para utility-scale é 2033. **[conferido]** |

## 2. O que baixar (em ordem de leitura)

O núcleo:

1. **arXiv:2606.03884**: Aghaee e outros 164 autores (Microsoft Quantum), *20 Second Parity Lifetime in an InAs–Pb Tetron Device*. v1 em 2/6/2026, v2 em 3/6/2026. Preprint, sem revisão por pares. É o "Majorana 2". **[conferido]**
2. **arXiv:2507.08795**: Aghaee e outros 165, *Distinct Lifetimes for X and Z Loop Measurements in a Majorana Tetron Device*. v1 em 11/7/2025, v2 em 4/9/2025. É de onde vem o τ_X que falta no Majorana 2. **[conferido]**
3. **Nature 638, 651–655 (2025)**: Microsoft Azure Quantum, *Interferometric single-shot parity measurement in InAs–Al hybrid devices*, doi 10.1038/s41586-024-08445-2. O "Majorana 1". A Nature bloqueou a leitura automática; baixe o PDF e o *peer review file*, e procure a nota editorial dizendo que o artigo não prova modos de Majorana. **[memória]** para a nota e para a data (19/2/2025).
4. **arXiv:2502.12252**: Aasen e outros, *Roadmap to fault tolerant quantum computation using topological qubit arrays* (fev. 2025). É a issue #14. **[conferido]**
5. **PRB 107, 245423 (2023)**, arXiv:2207.02472: *InAs-Al hybrid devices passing the topological gap protocol*. Define o TGP, que é o alvo de toda a crítica. **[conferido]**

A contestação:

6. **Legg, Nature (24/6/2026)**, *Matters Arising* sobre o artigo 3, e a **resposta da Microsoft** no mesmo número. DOIs: 10.1038/s41586-026-10567-8 e 10.1038/s41586-026-10568-7. A imprensa diverge sobre qual é qual (o Register cita o título *On the robustness of topological gap detection via transport* no 10568-7; o Hackaday diz que o 10567-8 é o do Legg). Baixe os dois. **[conferido em segunda mão]**
7. **Legg, arXiv:2502.19560** (26/2/2025): comentário sobre o PRB de 2023. O TGP não tem definição consistente de "gap" nem de "topológico" e depende das faixas de campo, tensão e resolução escolhidas. **[conferido]**
8. **Legg, arXiv:2503.08944** (mar. 2025): comentário sobre o artigo 3. O TGP pode classificar a mesma região como gapped ou gapless. **[conferido]**
9. **Frolov e Mourik**, análise dos dados do artigo de 2018, Zenodo 4587841. **[conferido]**

A teoria que veio depois do Majorana 2 (todos preprints, out. 2026 ou antes):

10. **arXiv:2608.27452**: Roy, Sau, Tewari (27/8/2026). Um segmento **normal** do fio pode produzir a mesma oscilação de capacitância quântica que se atribui ao Majorana; propõem um teste para separar os dois. É o argumento mais forte contra a leitura topológica. **[conferido]**
11. **arXiv:2610.12223**: Laubscher, Sau, Das Sarma (8/10/2026). Por que o τ_X medido sob leitura contínua pode ser muito maior que o T2* do tetron isolado. Relevante para o dia em que o X aparecer. **[conferido]**
12. **arXiv:2610.07169**: Stanescu, Tewari (5/10/2026). Propõe o tetron de um lado só. **[conferido]**

A genealogia (todos **[memória]**, conferir no PDF):

13. **Majorana (1937)**, *Teoria simmetrica dell'elettrone e del positrone*, Il Nuovo Cimento 14, 171. Some em março de 1938.
14. **Kitaev (1997)**, *Fault-tolerant quantum computation by anyons*, quant-ph/9707021 (Annals of Physics 303, 2, 2003).
15. **Kitaev (2000)**, *Unpaired Majorana fermions in quantum wires*, cond-mat/0010440 (Physics-Uspekhi 44, 131, 2001). A cadeia de Kitaev.
16. **Nayak, Simon, Stern, Freedman, Das Sarma (2008)**, *Non-Abelian anyons and topological quantum computation*, Rev. Mod. Phys. 80, 1083. A revisão de referência.
17. **Lutchyn, Sau, Das Sarma (2010)**, PRL 105, 077001, e **Oreg, Refael, von Oppen (2010)**, PRL 105, 177002. A receita: nanofio semicondutor + supercondutor + campo magnético.
18. **Mourik e outros (Kouwenhoven, Delft), Science 336, 1003 (2012)**. O primeiro pico de condutância em tensão zero.
19. **Zhang e outros, Nature 556, 74 (2018)**, *Quantized Majorana conductance*. Retratado em 8/3/2021 a pedido dos autores. A investigação de Delft não achou fabricação, mas achou seleção de dados. **[conferido: retratação e data]**

## 3. As contas (rodadas)

```
22 s / 12 ms  = 1833
22 s / 1 ms   = 22000
20 s / 1 µs   = 2e7 operações (a frase do vídeo em 1:50)
14,5 µs / 1 µs = 14,5 operações (o τ_X de 2025 com o mesmo critério)
```

O "1000x" é o piso conservador da comparação. A mesma régua que o vídeo usa para dizer "dezenas de milhões de operações", aplicada ao X de 2025, dá **14 operações**. O capítulo pode mostrar isso com uma frase.

A exponencial de 2:12: se a taxa de troca de paridade escala como exp(−Δ/k_B T_ef), passar de Δ = 30 para 70 µeV (ΔΔ = 40 µeV) dá 1000x quando k_B T_ef ≈ 5,8 µeV, ou T_ef ≈ 67 mK (1833x → 62 mK; 22000x → 46 mK). É uma temperatura efetiva plausível para quasipartículas num refrigerador de diluição. **Essa conta é minha, não do artigo**: antes de entrar no livro, conferir no 2606.03884 qual modelo eles usam para a dependência com o gap.

## 4. Linha do tempo

| Data | Fato | |
| --- | --- | --- |
| 1937 | Majorana: uma partícula que é a própria antipartícula | memória |
| mar. 1938 | Majorana desaparece | memória |
| 1997 | Kitaev: computar com ânions, protegido por topologia | memória |
| 2000–2001 | Cadeia de Kitaev: modos de Majorana nas pontas de um fio | memória |
| 2005 | Microsoft Station Q (Freedman); o vídeo fala em "20 anos" | memória |
| 2010 | Receita do nanofio (Lutchyn–Sau–Das Sarma; Oreg–Refael–von Oppen) | memória |
| 2012 | Mourik e outros: pico em tensão zero | memória |
| 2018 | Zhang e outros: "condutância quantizada" na Nature | memória |
| 8/3/2021 | Retratação | conferido |
| jul. 2022 / 2023 | Topological Gap Protocol (arXiv, depois PRB) | conferido |
| 19/2/2025 | Majorana 1 + artigo na Nature + roadmap | conferido (data: memória) |
| 26/2/2025 | Legg, primeiro comentário (TGP) | conferido |
| mar. 2025 | Legg, segundo comentário (Nature 2025) | conferido |
| 11/7/2025 | Preprint X e Z: τ_X = 14,5 µs, τ_Z = 12,4 ms | conferido |
| 2/6/2026 | Majorana 2: preprint 2606.03884, blog, Build, meta de 2029 | conferido |
| 24/6/2026 | Matters Arising do Legg e resposta da Microsoft na Nature | conferido (segunda mão) |
| ago.–out. 2026 | Respostas teóricas (Roy–Sau–Tewari; Laubscher–Sau–Das Sarma; Stanescu–Tewari) | conferido |
| 7/10/2026 | DARPA amplia o Stage C; Microsoft já estava lá desde o US2QC | conferido |
| 16/11/2026 | O vídeo | conferido |

## 5. Posição

- **O dado novo é real e é bom.** Uma paridade Z que dura 22 s num fio com chumbo é uma melhora grande de material, e o gap mais que dobrou. Isso é física de material, e ninguém contestou o número em si.
- **"Qubits 1000x mais confiáveis" é marketing.** O que foi medido é quanto tempo um bit clássico (a paridade) fica parado. Sem X, sem fidelidade de medição, sem porta, não há qubit demonstrado. É a crítica do Legg ("refers to the lifetime of a classical bit"), e ela está certa.
- **A frase mais errada do vídeo** é a de 1:47: "tens of millions of operations before an error". Pela mesma régua, o X de 2025 dá 14.
- **Topológico ou trivial continua aberto.** O Roy–Sau–Tewari mostra que um segmento normal imita o sinal. O histórico do programa (retratação de 2021, bugs no código do TGP admitidos como "minor off-by-one-pixel bug") justifica exigir mais do que de outra plataforma.
- **Mesmo se der certo**, Majoranas só fazem portas de Clifford por medição. A porta T vem de estados mágicos, como em qualquer plataforma (cap. 14 e o trecho de Gottesman–Knill do cap. 12). A proteção topológica compra o critério 3 e um overhead de correção menor, não a universalidade.
- **2029** é a meta da empresa. O que a DARPA fez foi pôr o projeto em verificação independente (Stage C), e a meta do próprio programa é 2033.

## 6. Esqueleto do capítulo 13 (proposta)

Título: algo como *A Bit That Lasts Twenty Seconds* ou *The Qubit Nobody Has Seen*. Rótulo: `ch:majorana`.

- **Etimologia**: Majorana (Ettore), ânion (Wilczek, 1982, de *any*), topologia (*topos* + *logos*), tetron (quatro modos), paridade.
- **A partícula que é a própria antipartícula**: caixa de história, 1937 · Roma/Nápoles.
- **A ideia do Kitaev**: guardar o qubit onde o ruído local não alcança. Caixa de conceito: proteção topológica (o que é, o que corrige: o critério 3 e o custo da Parte IV; o que custa: material exótico, não universal).
- **A receita de 2010 e o pico de 2012**.
- **2018–2021: a retratação**: caixa de história.
- **Majorana 1 e o TGP (2023–2025)**: o que a Nature publicou, a nota editorial, o Legg.
- **Majorana 2: o que mudou e o que foi medido**: Pb, InAsSb, gap de 30 para 70 µeV, τ_Z de 22 s. Caixa de reflexão: "como dobrar o gap dá 1000x" (a conta dos 67 mK, se o artigo confirmar o modelo).
- **O que o vídeo diz e o que o artigo diz**: caixa de pergunta: "um qubit de 20 segundos é melhor que um transmon de 1 ms?". Resposta: não é um qubit de 20 s, é um bit de 20 s; falta o X.
- **Se der certo**: porta T, distância até um problema útil, 2029 contra 2033.

Fora do capítulo:

- (Feito) Cap. 12, [linhas 509–514](../../book/chapters/12-what-a-qubit-is-made-of.tex#L509-L514) e a linha "topological" da tabela: hoje dizem "as of 2025"; acrescentar o `\ref{ch:majorana}`.
- Índice do [book/README.md](../../book/README.md).
- Uma issue de leitura para o 2606.03884, dependendo da #14, e o registro em `referencias/papers.md` quando a leitura fechar.

## Fontes lidas nesta sessão

- [Vídeo (YouTube)](https://www.youtube.com/watch?v=ytfzbmLCTas)
- [Blog da Microsoft, 2/6/2026](https://quantum.microsoft.com/en-us/insights/blogs/majorana-2-scalable-quantum-processor)
- [arXiv:2606.03884](https://arxiv.org/abs/2606.03884) · [2507.08795](https://arxiv.org/abs/2507.08795) · [2608.27452](https://arxiv.org/abs/2608.27452) · [2610.12223](https://arxiv.org/abs/2610.12223) · [2610.07169](https://arxiv.org/abs/2610.07169) · [2502.19560](https://arxiv.org/abs/2502.19560) · [2503.08944](https://arxiv.org/abs/2503.08944)
- [The Quantum Insider, 2/6/2026](https://thequantuminsider.com/2026/06/02/microsoft-reports-advances-in-majorana-2-following-debate-over-last-years-topological-claims/)
- [The Register, 24/6/2026](https://www.theregister.com/research/2026/06/24/boffin-claims-microsofts-supposed-quantum-leap-does-not-compute-due-to-basic-python-errors/5260489)
- [Hackaday, 30/6/2026](https://hackaday.com/2026/06/30/microsofts-topological-quantum-computing-claims-once-again-in-question/)
- [DARPA, 7/10/2026](https://www.darpa.mil/news/2026/four-more-teams-enter-quantum-benchmarking-initiative-final-stage)
- [Retraction Watch, 8/3/2021](https://retractionwatch.com/2021/03/08/authors-retract-nature-majorana-paper-apologize-for-insufficient-scientific-rigour)

Bloqueadas (baixar à mão): Nature (os três DOIs), Science (*Doubling down on controversial claims...*, 2/6/2026), PostQuantum.
