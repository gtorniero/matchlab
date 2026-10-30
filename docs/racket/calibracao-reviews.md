# Racket Match — calibração do índice contra reviews (out/2026)

## Dados do relatório PDF (23/out)
- Trechos de review: as 58 raquetes têm pelo menos 2, resumidos e traduzidos (testadores TW + Tennisnerd, Tennis Companion, The Tennis Tribe e outros). Versões leves usam reviews de outros sites ou média de clientes TW; gerações anteriores vêm indicadas.
- Atletas: 45 de 58 raquetes com profissionais por linha. Incluídos nesta rodada: Dunlop CX (Mérida, Brooksby, Jamie Murray, Santamaria), Dunlop SX (Vallejo), Prince Tour (Pouille, customizada). Sem profissional confirmado: Clash, Shift, Instinct, Ti S6, Boost Drive, ProKennex, Phantom, Ripstick. Burn (Pavlyuchenkova) ficou de fora por fonte fraca (jan/2025).
- Comparação com o Tennis Engineer no mesmo perfil (intermediário, cotovelo, Pure Strike 98): o top 3 deles (Shift 99, Extreme MP, Percept 100, todas 66–67 RA) fica entre 16º e 37º no nosso, por causa da dor no cotovelo; os dois motores concordam que vale trocar a Pure Strike.

## Rodada 5 — iniciante leve, zona sempre com raquete, Match legível e tensão (30/out)

Caso real: iniciante leve (perfil de mulher adulta, força abaixo da média). Peso ideal calculado 248 g → zona 240–256 g sem nenhuma raquete adulta no catálogo (a mais leve tem 260 g). Resultado: 1ª fora da zona, Match máximo 74% e 10º com 46%; tensão sugerida 55–57 lb com nylon.

Mudanças:
- Peso ideal com piso de 258 g para adulto (14 anos ou mais).
- Zona do mapa alarga aos poucos até ter pelo menos 3 raquetes do catálogo.
- A 1ª fica sempre na zona: a melhor da zona sobe para 1º se estiver até 10 pontos atrás.
- Escala do Match: a melhor para o perfil fica entre 90 e 96; as demais caem 0,8 ponto por ponto de diferença. A ordem do ranking não muda.
- Tensão (base): iniciante com nylon 54 → 50 lb e sem o +2 de "quero controle" (para iniciante, tensão baixa dá saída de bola e ponto doce maior); poliéster 51 → 48 lb; poliéster facetado (avançado com muito spin) 51 → 49 lb; híbrido para braço sensível 50 → 49 lb.
- Relatório abre com um parágrafo em linguagem simples dizendo por que aquela raquete.

Simulação com 500 perfis aleatórios:
| | Rodada 4 | Rodada 5 |
|---|---|---|
| 1ª dentro da zona | 75% | 99% |
| Match da 1ª (mín / p10 / mediana / máx) | — | 84 / 91 / 94 / 96 |
| Match da 10ª (mín / p10 / mediana / máx) | — | 61 / 73 / 81 / 93 |
| Raquetes diferentes em 1º | 31 | 32 |

Caso real depois: Head Boom Team 94% (dentro da zona 248–268 g), top 3 entre 86% e 94%, tensão 48–50 lb.

## Rodada 4 — mapa e ranking coerentes (28/out)

Problema visto em teste real: o relatório recomendava raquete fora da "sua zona" no mapa peso × swingweight. A zona desenhada (peso ideal ±8 g, swingweight ideal ±6) era mais estreita do que o motor cobrava: abaixo da zona, o swingweight só era penalizado 6 pontos depois da borda, e o peso tinha penalidade leve (1/3 por grama).

Simulação com 500 perfis aleatórios (todas as respostas sorteadas):
| Versão | 1ª dentro da zona | Fora da zona havendo raquete dentro | Raquetes diferentes em 1º | Clash 100 v3 em 1º |
|---|---|---|---|---|
| Antes | 27% | 63% | 33 | 40% |
| Penalidade a partir da borda (1,2 por g ou ponto de SW) | 41% | 48% | 28 | — |
| **Publicado: penalidade da borda + zona no Match (±4 pontos)** | **75%** | **15%** | **31** | **14%** |

Regra no motor:
- Peso e swingweight passam a ser penalizados a partir da borda da zona do mapa (1,2 por grama ou ponto de swingweight).
- Estar dentro da zona soma 4 pontos ao Match; fora, tira 4.
- Quando a 1ª ainda fica fora da zona (sem raquete na zona, ou as da zona são bem piores por rigidez, preço etc.), o relatório diz por quê: qual a melhor dentro da zona, quantos pontos atrás e o motivo.
- Exemplo pronto passa a preferir comprar no Brasil (antes recomendava a Black Ace 105, sem loja no Brasil).

Limite: não foi refeita a validação com os 30 testadores da TW (os dados brutos não estão no repositório). Refazer quando a base voltar.

## Rodada 3 — 30 perfis, destro/canhoto, backhand e Clash (23/out)

### Evidência: o que muda a recomendação
| Fator | Conclusão | Força da evidência | Regra no motor |
|---|---|---|---|
| Canhoto vs destro | Não muda nada: raquete é simétrica; nenhum varejista, review ou estudo recomenda spec diferente | Moderada (ausência consistente) | Peso zero. Só dica no relatório: canhoto enrola o overgrip no sentido contrário (Tennis Warehouse) |
| Backhand de 1 mão (int/avançado) | Consenso de especialistas: mais massa e swingweight, quadro com balanço na mão, cabeça 97–100. Pros de 1 mão usam ~8 g a mais (amostra pequena) | Fraca / prática | +5 no swingweight ideal, empurrão leve em estabilidade, +3 g só para avançado, leve penalidade para balanço >325 mm. Nada para iniciante |
| 1 mão e cotovelo | Associação fraca e contraditória (Song et al., 402 jogadores, a favor; estudo com 2.633 alunos, contra). O mesmo estudo não associou rigidez, peso ou tensão à epicondilite | Fraca | 1 mão sozinho não muda nada; com cotovelo sensível, penaliza quadro < 295 g |

Fontes: tenniswarehouse-europe.com/LC/Regripping.html · tennisnerd.net (best racquets one-handed backhand) · toomanyrackets.com (one-handed backhands; average weight of pro rackets) · newswise.com (modern tennis trends, tennis elbow) · experts.umn.edu (The Elbow and Tennis, part 1) · Clin Sports Med 1995 (biomechanics of tennis elbow) · PMC4950282 (Mohandhas 2016, tensão e aceleração no cotovelo).

### Teste com 30 perfis diversos (iniciante a 4.5, 14 a 62 anos, dor em cotovelo, ombro e punho, 1 e 2 mãos, canhoto, orçamento baixo, raquete atual pesada/leve)
- Inverter canhoto/destro nos 30: top 3 muda em 0 de 30 (antes também 0).
- Inverter backhand 1↔2 mãos: top 1 mudava em 10 de 30 (efeito forte demais para evidência fraca) → agora 4 de 30.
- Clash 100 em 1º: 4 de 30, todos com dor no braço ou pós-lesão. É o consenso das reviews (RA 54, conforto nº 1 na TW). Rigidez ficou menos punitiva (cotovelo ×3 → ×2,2; punho/ombro sem cotovelo, limite 65 RA), o que abre espaço para Gravity MP, Phantom 100X, Speed MP e VCORE 98 nesses perfis.
- 14 raquetes diferentes em 1º lugar entre 30 perfis; diferença média 1º–10º: 10,7 pontos.

### Validação com os 30 testadores da TW (deixando o testador fora da base)
| Versão | Correlação média | Acerta a favorita | Favorita no top 2 |
|---|---|---|---|
| Rodada 2 | 0,33 | 5/28 (18%) | 13/28 |
| Sem aprovação TW | 0,25 | 7/28 | 15/28 |
| Aprovação ×3 para todos | 0,36 | 9/28 | 15/28 |
| **Publicado (rodada 3)** | **0,33** | **8/28 (29%)** | **16/28** |
Acaso = 14%.

Trade-off decidido: aprovação TW forte para todos melhora um pouco a validação, mas coloca a Pure Aero 98 no top 3 de 27 dos 28 testadores e de 14 dos 30 perfis (efeito popularidade). Versão publicada:
- Aprovação pesa por nível (avançado 2,5×, 4.0 2×, intermediário 1×, iniciante 0,6×), porque os testadores TW são 4.5+.
- Aprovação só desempata entre raquetes que já estão perto do perfil (some quando a distância passa de 1,2 acima da melhor).
- Bônus de "Braço Seguro" reduzido (era contado três vezes: alvo de conforto, bônus e penalidade de rigidez).
- Teto de swingweight por nível (iniciante 312, intermediário 320, 4.0 326).
- Novo: salto de mais de 35 g em relação à raquete atual é penalizado (troca em etapas).

### Gaps que continuam
- Validação só cobre jogadores avançados (testadores TW). Iniciantes e intermediários não têm verdade de campo: precisa de pesquisa com jogadores reais (30–50 respostas + raquete que aprovam).
- Personas de testadores são inferidas (nível, estilo, raquete) e quase todas parecidas (25 avançados, força alta): limita a diversidade possível do top 3.
- Versões leves seguem sem reviews TW.

## Rodada 2 — Tennis Warehouse (base principal)
- 670 avaliações da Tennis Warehouse: 545 notas individuais de testadores (geração atual + até 3 anteriores do mesmo modelo, ~4 testadores por review) e 125 reviews de clientes.
- Por raquete: 24 com 15+, 20 com 8–14, 9 com 1–7, 5 sem nada (Pure Aero Lite, Pure Drive Lite, Boost Drive, Speed Team, Blade 100L). TW não faz review das versões leves; as reviews de clientes dos produtos atuais não carregam sem navegador.
- Gerações mais antigas pesam menos (atual 1,0; até 2 anos 0,65; até 4 anos 0,4; mais velhas 0,2). Clientes pesam 0,3.
- Cada nota foi corrigida pela régua do testador: usamos o formato do perfil de cada avaliação (nota do atributo menos a média da própria avaliação) e a aprovação relativa à média daquele testador.

### Concordância de perfil com a TW (Spearman, 43 raquetes com 3+ avaliações)
| Atributo | Índice antigo | Índice novo | Outros sites vs TW |
|---|---|---|---|
| Potência | 0,71 | 0,72 | 0,87 |
| Controle | 0,77 | 0,76 | 0,87 |
| Spin | 0,67 | 0,74 | 0,67 |
| Conforto | 0,62 | 0,68 | 0,84 |
| Manobra | 0,72 | 0,71 | 0,73 |
| Estabilidade | 0,73 | 0,73 | 0,78 |
Os outros sites concordam fortemente com a TW: o sinal das reviews é consistente.

### Validação por testador
30 testadores avaliaram 3+ raquetes (512 avaliações). Teste honesto, excluindo o próprio testador da base.
| Versão do motor | Correlação com a aprovação do testador |
|---|---|
| Original (só specs) | 0,09 |
| Publicado na rodada 1 (specs + sites) | 0,08 |
| Specs + perfil TW | 0,175 |
| Specs + perfil TW + aprovação TW | 0,345 |

### Achados por nível
- Testadores 4.5/Open: aprovam mais raquetes com mais swingweight e peso (+0,16/+0,17).
- Testadores até 4.0: leve preferência por quadros mais macios e cabeça não muito grande (−0,11 / −0,13).

### O que mudou no motor (rodada 2)
- Raquete com 3+ avaliações TW: perfil puxado para o da TW com peso de 25% + 3% por avaliação (máximo 70%). Senão, vale o ajuste da rodada 1.
- Aprovação TW no Match Score (ajustada na rodada 3).

## Rodada 1 — reviews globais (resumo)
- 145 reviews de 13 sites (125 usadas). Rigidez pesava demais na potência; spin depende mais de padrão aberto e linha de spin; conforto ganha com massa; estabilidade é sobretudo swingweight; tecnologia de amortecimento quase não aparece nas notas.
- Efeito halo: raquete querida ganha nota alta em tudo; usamos o formato do perfil e tratamos a aprovação à parte.

## Pendências e oportunidades
- Versões leves (L, Lite, Team, Boost) seguem só com specs: ler reviews de clientes da TW com navegador ou fóruns (TT Talk, r/10s) com peso baixo.
- Dados que misturam variações (Phantom 305 g, TF40 18x20, CX 200 Tour 18x20, Ki Q+ 305/315) e gerações antigas: filtrar se a base crescer.
- 7º atributo de toque/voleio (TW Touch/Feel e Volleys) e notas por golpe (saque, devolução) para casar com as perguntas de saque e estilo.
- Validação real: aplicar o teste a 30–50 jogadores e comparar com a raquete que eles aprovam (principal gap para iniciante/intermediário).
