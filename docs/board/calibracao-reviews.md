# Board Match — calibração do motor contra casos reais (out/2026)

## Base: 422 casos (390 usados; 32 sem nível ou tipo)
| Frente | Casos | Peso + litragem | Fontes principais |
|---|---|---|---|
| Lojas (reviews de usuários) | 79 | 67 | Boardcave 72, Hawaiian South Shore 6 |
| Revistas e especialistas | 97 | 45 | Stab 45, The Inertia 20, Empire Ave 17, Swellnet 7, Surf Simply 4 |
| Marcas e coaches (tabelas e calculadoras) | 88 | 88 | Surf Simply, NSP, calculadora Guild Factor, Fly Surf, Rapture, Softech, Catch Surf |
| Atletas | 89 | 66 | JS Industries 48, Stab 14, WSL, Volcom |
| Fóruns | 69 | 25 | Seabreeze 66 |

Método: cada caso virou um perfil do questionário (peso, altura, nível, ondas, estilo) e rodou no motor publicado. 30% dos casos ficaram separados para validação (sorteio fixo por id) e não foram usados no ajuste.

## Resultado
| Métrica (390 casos) | Antes | Depois |
|---|---|---|
| Tipo certo em 1º | 44% | 56% |
| Tipo certo no top 3 | 71% | 77% |
| 1º certo ou tipo vizinho | 77% | 81% |
| Litragem a ±10% do que a pessoa usa (n=257) | 33% | 56% |
| Litragem a ±15% | 55% | 72% |
| Erro absoluto mediano de litragem | 13,7% | 8,6% |

Validação (122 casos fora do ajuste): 1º certo 64%, top 3 80%, litragem a ±15% em 72%.

## Litros por kg observados (casos reais, veredito positivo)
Pro 0,365 (pranchinha), 0,41 (step-up) · Avançado 0,375–0,41 · Intermediário 0,41 (pranchinha) a 0,47 (evolution/mid) · Já fica de pé 0,50–0,56 · Iniciante em soft: tabelas indicam mínimo de 0,8.

## O que mudou no motor
- Fatores de litragem por nível: já fica de pé 0,58→0,47; intermediário 0,45→0,41; intermediário avançado 0,41→0,385; avançado 0,385→0,36.
- Multiplicador por tipo: mini-malibu 1,8; mid 1,25; evolution 1,1; step-up 1,11; gun 1,3; biquilha 1,0.
- Saíram descontos que puxavam a litragem para baixo sem base (condicionamento forte, onda grande, frequência alta). EPS desconta 1 L (antes 2).
- Afinidades por nível e objetivo: evolution menos dominante para intermediários; groveler sobe para intermediários em onda pequena; mini-malibu mais forte para quem já fica de pé; longboard ganha no objetivo "curtir sem pressão".
- Softboard ganha força para quem ainda não fica de pé.
- Pergunta nova: "Você quer uma prancha de espuma (soft)?" (resolve softboard de performance). Depois passou a aparecer só para quem está começando.

## Limites e próximos passos
- Fish e biquilha ainda erram (0/8 e 4/14 no top 3): são escolha de estilo; os casos raramente dizem o estilo do surfista. Testar com usuários reais que escolhem "deslizar com velocidade".
- Longboard, gun e step-up têm poucos casos com tamanho de onda. Faltaram Joel Tudor, Kassia Meador e guns de onda grande (limite de buscas).
- Litragem de soft para iniciante sai ~25% acima das tabelas de mínimo; mantido de propósito (softs reais de 8' têm 70–86 L). Validar com o Gustavo.
- Base enviesada para Austrália (Boardcave, Seabreeze) e JS Industries nos atletas. Próxima rodada: lojas BR, Surfboard Empire, Degree 33, Reddit, e 30–50 alunos reais do Gustavo.

## Rodada 2: coerência e teste de fogo (24/out/2026)
Sem casos novos; correções de regra encontradas testando perfis-limite no motor publicado.
- **Softboard +12** quando o tempo de surf é de até 6 meses e a pessoa marca até 2 habilidades (correção do `docs/teste-de-fogo.md`, que ainda não estava no motor). Antes, um iniciante de 3 meses que já pega espuma sozinho caía em mini-malibu.
- **Prancha para dias grandes** (papel no quiver): pranchinha −8, step-up +4. Antes, um avançado que pedia prancha para dias grandes recebia pranchinha em 1º.
- **Onda acima de 2,5 m**, só para intermediário avançado e avançado: gun +14, pranchinha −4. Antes, o gun ficava em 4º mesmo com onda grande, laje e prancha para dias grandes; agora fica em 2º, atrás do step-up.
- **Groveler em onda de 1,5 m para cima**: −6. Antes, um intermediário que gosta de manobra recebia groveler em onda de 1,5 a 2,5 m; agora recebe evolution.
- O perfil do "Ver um exemplo pronto" não mudou (Mid-length 96%, 37,6 L).
- Não houve nova medição nos 422 casos (a base não está no repositório). Rodar de novo na próxima rodada, junto com os 30–50 alunos do Gustavo.

## Rodada 3: questionário e litragem de avançado (25/out/2026)
Ajustes pedidos depois do teste do dono do projeto (avançado, dor no ombro, recebeu groveler de 28 L com uma evolution de 30 L).
- **Pergunta nova: dor ou lesão** (ombro, joelho/quadril, lombar, mobilidade; pode marcar mais de uma). Litros a mais: ombro +2,5 L; joelho/quadril +1,5 L; mobilidade +1,5 L; lombar +1 L. Joelho, quadril ou mobilidade puxam para tipos mais estáveis; ombro e lombar, um pouco. O relatório mostra aviso de saúde (fisioterapeuta).
- **Avançado:** fator de litragem de 0,385→0,36 para 0,40→0,37 L/kg. O mínimo antigo ficava abaixo do observado nos casos reais de avançado (0,375–0,41) e igual ao de profissional (0,365).
- **Groveler:** multiplicador de volume 1,06 → 1,10. Groveler costuma ter igual ou mais volume que a pranchinha da pessoa.
- Resultado no perfil de teste (75 kg, avançado, onda pequena): groveler de ~28,6 L para 31,8 L sem dor e 34,3 L com dor no ombro.
- **Saíram as perguntas** de roupa (lycra/john) e de fundo do pico. Valem o padrão: sem ajuste de roupa e beach break.
- **"Onde vai usar" e "papel da prancha" viraram uma pergunta só:** "Para que vai usar essa prancha?" (única, dias pequenos, dias grandes, viagem, piscina, mar e piscina).
- O questionário passou de 20–25 para 18–23 perguntas. O "Ver um exemplo pronto" não mudou (Mid-length 96%, 37,6 L).
- A validar com o Gustavo: os litros a mais por dor e a nova faixa de avançado.

## Rodada 4: coerência entre zona ideal e ranking (28/out/2026)
Mesma checagem feita no Racket Match (lá, só 27% dos 1º lugares caíam dentro da zona do mapa). Simulação com 500 perfis aleatórios no motor publicado (respostas sorteadas em todas as perguntas, peso 45–110 kg, altura 150–200 cm, metade com medidas da prancha atual).
- **Zonas que o Board mostra:** faixa de litros ("quanto ela deve boiar", na prévia, no Passo 2 e no PDF) e a régua do catálogo no PDF (comprimento ±2", largura ±1/4", espessura ±1/8", litros). O mapa do catálogo (comprimento × litros) não desenha zona.
- **Resultado:** o 1º lugar fica dentro de todas as zonas em 500 de 500 perfis (100%), e o 1º do ranking de 13 tipos é sempre a prancha recomendada. As zonas são calculadas a partir da própria recomendada (litragem do motor para o tipo vencedor ± a margem do nível), então não há como o 1º contradizer o gráfico. **Motor sem mudança.**
- **Para acompanhar (sem mudança agora):** o 2º e o 3º lugar caem dentro da faixa de litros do 1º em só 9% dos perfis (46 e 45 de 500), porque cada tipo tem a sua litragem; o relatório já mostra os litros de cada finalista. E o 1º lidera a prioridade nº 1 da pessoa (entre as 3 finalistas) em 48% dos perfis (242 de 500): o tipo pesa nível, estilo e onda antes das notas de prioridade, e a página 4 do PDF explica o que cada uma lidera e cede.
- Distribuição do 1º nos 500 perfis: mini-malibu 127, soft 78, mid 77, groveler 46, longboard 45, fish 22, twin 23, longboard performance 22, pranchinha 28, evolution 20, softp 6, step-up 5, gun 1.
