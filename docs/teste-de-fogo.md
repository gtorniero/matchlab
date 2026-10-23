# Teste de fogo dos motores (out/2026)

146 reviews de especialistas (50 raquetes, 50 pranchas, 46 tênis) viraram perfis do questionário e rodaram nos motores publicados.

| | Racket | Board | Tenis |
|---|---|---|---|
| Top 3 (atual → corrigido) | 44% → 44% | 68% → 80% | 54% → 70% |
| 1º lugar | 18% → 20% | 30% → 42% | 20% → 26% |
| Sorteio top 3 | 10% | 23% | 9% |
| Categoria certa | – | – | 72% → 91% |

## Correções a levar para cada app
- **Racket:** Gravity MP tem cabeça 100 (estava 104). Índice de conforto: `.5*(1-s)+.2*m+.1*hl+.2*cl((head-98)/17,0,1)` (área de batida conta). Falta desempate entre raquetes "spin agressivo" (Pure Aero, Shift 99, VCORE, SX 300, Speed MP): 94% dos casos ficam a ≤3 pts do 3º. Novas perguntas: sensação preferida (flexível/firme), marca, raquete atual; trazer swingweight medido.
- **Board:** softboard +12 quando tempo ≤1 e ≤2 habilidades. Novas perguntas: quer espuma (softp) e estilo clássico/andar na prancha (longp). Litragem não testada; validar com alunos do Gustavo.
- **Tenis:** se prova>0, nível ≥3, pares ≥1 e <85 kg → supertênis +9 (e rápido +3 se objetivo ≤10 km). Ultraboost 23, Supernova Glide e Inverse 2 sem review: validar com treinador.

## Limites
Correções feitas nos mesmos casos (resultado otimista); próxima rodada com 50 reviews novas por app. Perfis interpretados das reviews.
