# Racket Match — benchmark de concorrentes (out/2026)

## Mapa (20 + extras)
| # | Ferramenta | Modelo | Perguntas | Catálogo | Destaque |
|---|---|---|---|---|---|
| 1 | TW Racquet Finder (racquetfinder.com) | Varejo | Filtros mín./máx. de 8 specs | ~45 marcas | Lista filtrada, sem gráfico |
| 2 | TW Racquet Selector | Varejo | Nível/NTRP | 12 marcas | Lista por nível |
| 3 | TWU Racquet Comparison | Grátis | 2 dropdowns | >1.000 | A vs B lado a lado |
| 4 | TWU Racquet Analyzer | Grátis | Filtros | Laboratório | Dispersão swingweight × métrica, quadrantes, mapa de calor do encordoamento |
| 5 | TWU Recommender/Similar | Grátis | Raquete de referência | Laboratório | "Parecidas" |
| 6 | TW Reviews | Varejo | — | — | Notas 0–100 em 13 critérios, faixas RDC |
| 7 | HEAD Racquet Finder | Marca | 6 | Só HEAD | — |
| 8 | Tennis Express Quiz | Varejo | ~60 s | Loja | — |
| 9 | Wilson Find my Racket | Marca | 0 (guia estático) | Wilson | — |
| 10 | Babolat Play Test | Marca | Filtros | 3 linhas | Test-drive de 3 raquetes |
| 11 | Racqix | Afiliado | Quiz | n/d | Diferenças entre specs |
| 12 | FindMyRacket (DE) | Afiliado + premium | até 10 specs | n/d | Tem PT, foco Alemanha |
| 13 | Find My Racquet | n/d | 60 s | n/d | Raquetes de pros |
| 14 | AceFinder (UK) | Assinatura £5,99/mês | Inclui lesão | 75+ | Raquete + corda/tensão |
| 15 | RacketIQ | Afiliado Amazon | Poucas | 47 raquetes, 34 cordas | Conforto, tensão |
| 16 | RacketWise | Afiliado Amazon | n/d | n/d | Raquete + corda |
| 17 | Racketpedia StringAI | Assinatura | 9 (dor por articulação) | Laboratório | Só corda |
| 18 | iq.tennis | Afiliado | Sem quiz | 70 | Radar, barras, "range views" |
| 19 | String&RacketFinder | Grátis | Busca | 155 | 11 eixos 0–10 |
| 20 | RacketFit | Grátis | Quiz | Dados TWU | Raquete + corda + grip |
| + | Padel Rackets (app) | Anúncios | 4 | 1.700+ | 5 eixos, compara 3 |
| + | Pongbot Tension Calc | Isca de loja | 7 | — | Tensão explicada ajuste a ajuste |
| + | my-best BR | Afiliado | 0 | 10 | Ranking editorial |

## Similaridades
- Grátis + afiliado/varejo domina; só AceFinder e Racketpedia cobram, e por assinatura.
- Quiz curto (4 a 10 perguntas) e saída em lista ranqueada, sem o porquê.
- Mesmo vocabulário: power, control, spin, comfort, stability, maneuverability.
- Finders de marca só recomendam o próprio catálogo.

## Gaps
1. Nada interativo em PT-BR para o Brasil.
2. Dor no braço vira checkbox; ninguém tem índice visível e explicado.
3. Ninguém compara de verdade "sua atual vs recomendada".
4. Ninguém explica o encaixe.
5. Sem preço em R$.
6. Sem card para compartilhar.
7. O dado mais rico (swingweight do TWU) fica em telas de engenheiro.

## Oportunidades (aplicadas na v2 do Racket Match)
- Relatório avulso via Pix (ninguém faz) com prévia rica e borrada.
- Braço Seguro como marca própria, com medidor antes → depois e articulação da dor.
- Atual vs recomendada com deltas por spec (+/− SW, RA, peso).
- Tensão explicada ajuste a ajuste (estilo Pongbot).
- Preço estimado em R$ e geração anterior/usada.
- Card de story 9:16 baixável.

## Visuais que funcionam
1. Barras de spec com faixa do catálogo + zona ideal + marcador atual/recomendada (prioridade 1).
2. Hexágono sobreposto (ideal tracejado, recomendada preenchida, atual contorno).
3. Mapa peso × swingweight com zona ideal, quadrantes rotulados e seta da atual para a recomendada.
4. Silhueta geométrica da raquete em escala (cabeça, padrão, ponto doce, balanço) em vez de foto de marca.
5. Medidor semicircular do Braço Seguro.

## Próximos passos possíveis
- Padel: demanda clara (app com 1.700+ raquetes), nenhum concorrente com relatório.
- Disponibilidade no Brasil por modelo ("difícil de achar → alternativa").
