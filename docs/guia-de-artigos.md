# Match Lab — especificação dos artigos

Match Lab é um site brasileiro que ajuda a pessoa a achar o equipamento certo para o próprio corpo, nível e estilo. Tem três áreas: **Raquete Certa** (raquete de tênis), **Tênis Certo** (tênis de corrida) e **Prancha Certa** (prancha de surf). Cada área tem um teste (quiz) que recomenda o equipamento. Os artigos educam o leitor e levam ao teste.

## Tom
- Português do Brasil, claro, direto, de especialista conversando com amador interessado.
- Frases curtas, voz ativa. Nada de clichê de marketing, nada de "neste artigo vamos ver".
- Sem travessão como aparte; sem "não é X, é Y"; sem exclamações em excesso.
- Use os termos técnicos reais do esporte e explique cada um na primeira vez.
- Neutro com marcas: pode citar marcas e modelos como exemplos históricos ou de tecnologia, nunca como recomendação de compra. Não cite preços.
- Não invente estatísticas, estudos ou números precisos que você não tenha certeza. Prefira faixas usuais conhecidas (ex.: "a maioria das raquetes adultas fica entre 98 e 100 pol²"). Quando houver incerteza, fale em termos qualitativos.
- Segurança: quando falar de lesão, oriente a procurar profissional; não dê diagnóstico.

## Tamanho
Cada artigo com 550 a 800 palavras no corpo.

## Formato do arquivo
Um arquivo JavaScript que define uma variável global. Exemplo para raquete:

```js
window.ML_ARTICLES = window.ML_ARTICLES || [];
window.ML_ARTICLES.push(
{
  id: "raquete-01",            // prefixo da área + número com 2 dígitos
  area: "raquete",             // "raquete" | "tenis" | "prancha"
  cat: "escolher",             // "escolher" | "importancia" | "evolucao" | "tecnologia"
  title: "Como escolher sua primeira raquete de tênis",
  dek: "Uma frase de 15 a 25 palavras que resume o que a pessoa vai aprender.",
  level: "Iniciante",          // "Iniciante" | "Intermediário" | "Avançado" | "Todos"
  minutes: 5,                  // tempo de leitura estimado (palavras/200, arredondado)
  tags: ["peso", "cabeça"],    // 2 a 4 tags curtas em minúsculas
  body: [
    { t: "p", x: "Parágrafo." },
    { t: "h", x: "Subtítulo" },
    { t: "ul", items: ["Item", "Item"] },
    { t: "spec", caption: "Faixas típicas", rows: [["Peso sem corda", "255–285 g"], ["Cabeça", "98–105 pol²"]] },
    { t: "tip", x: "Dica prática destacada, uma ou duas frases." },
    { t: "quote", x: "Frase-síntese do artigo, curta, autoral (não atribua a ninguém)." }
  ]
},
...
);
```

Regras do corpo:
- Comece com 1–2 parágrafos `p` (sem subtítulo antes).
- Use 3 a 5 subtítulos `h`.
- Cada artigo deve ter pelo menos um `spec` OU um `ul`, e exatamente um `tip`. `quote` é opcional (no máximo um).
- Em `spec`, use as unidades reais do esporte (pol², g, kg, lb, mm, pés e polegadas, litros etc.).
- Não use markdown dentro dos textos. Pode usar **nada** de HTML. Texto puro.
- Strings com aspas duplas devem estar escapadas corretamente. O arquivo precisa ser JS válido: confira com `node -e "require('./ARQUIVO')"` usando um `global.window = {}` antes, por exemplo: `node -e "global.window={}; require('/caminho/arquivo.js'); console.log(window.ML_ARTICLES.length)"`.

## Distribuição de categorias (15 por área)
- 5 de `escolher` (como escolher)
- 3 de `importancia` (por que escolher certo importa: desempenho, lesão, evolução, dinheiro)
- 3 de `evolucao` (evolução do esporte e do jogador/surfista/corredor: história do equipamento e como o equipamento acompanha a evolução de nível)
- 4 de `tecnologia` (materiais, construções, tecnologias)

Os 15 temas precisam ser diferentes entre si e cobrir o assunto de ponta a ponta.
