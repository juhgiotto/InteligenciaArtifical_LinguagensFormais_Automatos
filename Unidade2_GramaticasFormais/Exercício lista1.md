Exercício 1 

Considere:

Σ = a, b, c

Responda:

- Quantos símbolos existem no alfabeto? 3 simbolos

- Quais são os símbolos? a,b e c

- O símbolo a pertence ao alfabeto? Sim

- O símbolo d pertence ao alfabeto? Não

- Escreva uma palavra formada por símbolos desse alfabeto. Abacaba

Exercício 2

Considere:

Σ = 0,1

Classifique cada sequência como palavra válida ou não válida:

|Sequência|Válida?|Justificativa|
|-|-|-|
|0101|Sim|Pertence ao alfabeto|
|00110|Sim|Pertence ao alfabeto|
|012|Não|O símbolo 2 não pertence ao alfabeto|
|111|Sim|Pertence ao alfabeto|
|10a|Não|O símbolo a não pertence|

Exercício 3

Considere:

Σ = 0,1

Determine se as afirmações são verdadeiras ou falsas:

0 ∈ Σ

1 ∈ Σ

01 ∈ Σ 

01 ∈ Σ∗

2 ∈ Σ

101 ∈ Σ∗

Justifique cada resposta.

|Sequência|Válida?|Justificativa|
|-|-|-|
|0 ∈ Σ|Sim|Pertence ao alfabeto.|
|1 ∈ Σ|Sim|Pertence ao alfabeto.|
|01 ∈ Σ|Não|O alfabeto possui apenas 0 e 1 e não o conjunto.|
|01 ∈ Σ∗|Sim|É uma palavra que é possível ser formada.|
|2 ∈ Σ|Não|O símbolo 2 não pertence ao alfabeto.|
|101 ∈ Σ∗|Sim|É uma palavra que é possível ser formada.|

Exercício 4

Considere:

L=0, 01, 011, 0111

Determine se cada palavra pertence à linguagem:

0 ∈ L

01 ∈ L

0111 ∈ L

10 ∈ L

111 ∈ L

011 ∈ L

|Sequência|Válida?|Justificativa|
|-|-|-|
|0 ∈ L|Sim|Pertence ao alfabeto.|
|01 ∈ L|Sim|Pertence ao alfabeto.|
|0111 ∈ L|Sim|Pertence ao alfabeto.|
|10 ∈ L|Não|A palavra não pertence ao alfabeto.|
|111 ∈ L|Não|A palavra não pertence ao alfabeto.|
|011 ∈ L|Sim|Pertence ao alfabeto.|

Exercício 5

Considere:
L=bn∣n≥1

- Escreva as cinco primeiras palavras.
Para n=1,2,3,4,5

b1 = b

b2 = bb

b3 = bbb

b4 = bbbb

b5 = bbbbb

Resposta: b, bb, bbb, bbbb, bbbbb.

- Explique o significado de bn.

A expressão b^n significa que o símbolo b é repetido n vezes.
Como n≥1 a quantidade de símbolos b deve ser pelo menos 1.

- A palavra bbbbbb pertence à linguagem?

A palavra bbbbbb possui 6 símbolos b, ou seja:

bbbbbb = b^6

Como 6≥1 a palavra pertence à linguagem.

- A palavra vazia (ε) pertence à linguagem?

Não, pois n precisa ser maior que 1.

Exercício 6

Explique, com suas próprias palavras, a diferença entre:
L=∅
L=ε

L=∅ significa que a linguagem é vazia. Ela não contém nenhuma palavra.
L={ε} significa que a linguagem contém uma única palavra, que é a palavra vazia ε.

Depois responda:

- Qual delas possui uma palavra? A segunda.
- Qual delas não possui nenhuma palavra? A primeira.
- Qual é o comprimento da palavra ε? 0 símbolos.

Exercício 7

Considere:
G=(S,A,0,1,P,S)
com:
P=S→0A, A→1

Identifique:
- O conjunto de variáveis. V = {S, A}
- O conjunto de terminais. T = {0, 1}
- O conjunto de produções. P = {S → 0A, A → 1}
- O símbolo inicial. S
- Qual palavra pode ser gerada por essa gramática? 01

Exercício 8

Considere:
S→0S
Começando com S:

- Aplique a regra uma vez. S → 0S
- Aplique a regra duas vezes. S → 0S → 00S
- Aplique a regra três vezes. S → 0S → 00S → 000S
- Escreva a sequência completa de derivação. S → 0S → 00S → 000S


Exercício 9 

Utilizando:
G:{S→aSS→b
gere:
aaab
Escreva todos os passos da derivação.

S → aS → aaS → aaaS → aaab

Exercício 10 

Considere novamente:
G:{S→0SS→1

Determine se cada palavra pode ser gerada:

Para as palavras que podem ser geradas, apresente a derivação completa.

|Sequência|Pode ser gerada?|Justificativa|
|-|-|-|
|1|Sim|Faz parte da derivação.|
|01|Sim|Faz parte da derivação.|
|001|Sim|faz parte da derivação.|
|0001|Não|Faz parte da derivação.|
|101|Não|Não faz parte da derivação.|
|1001|Não|Não faz parte da derivação.|


