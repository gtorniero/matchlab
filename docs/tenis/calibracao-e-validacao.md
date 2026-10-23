# Tenis Match — calibração e validação com reviews (out/2026)

## Rodada 2: validação com reviews profissionais
- 8 agentes percorreram os 231 tênis. Só reviews profissionais com teste real ou de laboratório (RTINGS, RunRepeat, Doctors of Running, Road Trail Run, Believe in the Run, Running Shoes Guru, The Run Testers, Solereview, Running Warehouse, iRunFar, OutdoorGearLab, Tom's Guide e blogs BR com teste real para a Olympikus).
- +293 reviews novas em 138 modelos. Base: 795 → **1.088 reviews**.
- Sem review profissional (46 modelos): quase todos de entrada (Olympikus Pride, Veloz, Volta, Corre Trilha; Mizuno de entrada; ASICS só do Brasil; Fila; 361°; NB 520, 680 e Arishi).

| Atributo | Concordância de ranking (Spearman) | Erro médio (1–5) | Desvio entre as próprias fontes |
|---|---|---|---|
| Resposta | 0,75 | 0,52 | 0,55 |
| Estabilidade | 0,56 | 0,59 | 0,49 |
| Maciez | 0,53 | 0,58 | 0,46 |
| Aprovação geral | 0,40 | 0,36 | 0,41 |

O erro do catálogo é do mesmo tamanho da discordância entre os próprios reviewers.

**Maiores correções:** Takumi Sen 11 mais estável e menos macio; Cloudboom Strike 2 mais estável, mais firme e menos responsivo; Tempus 2, Caldera 8, Adizero Evo SL e Ultraboost 5 mais macios; Metaspeed Edge Tokyo e Zoom Fly 6 mais estáveis; Megablast mais firme; Ghost Max 3 mais macio e menos estável; Sonicblast e Superblast 3 menos responsivos.

**Mudanças no motor:** consenso ponderado (review nova pesa 1, laboratório 1,2); specs pela mediana das medições de laboratório; etiquetas de uso e de contraindicação quando 2+ reviews citam; aviso de divergência entre fontes em 29 modelos ("As reviews profissionais discordam sobre… Vale provar antes de comprar.").

**Teste com 10 perfis:** top 3 adequado 30/30; uso e perfil juntos 28/30. Maratona competitiva: Adios Pro 5, Metaspeed Edge Tokyo, Deviate Nitro Elite 4. Pronador: GT-2000 15, Wave Inspire 22, Structure 26.

**Pendências:** limpar fontes de geração errada (Aero Glide 4, Kinvara 16, Peregrine 16, Endorphin Pro 5, Velociti Elite 2); atualizar Tecton X 4, Infinite Pro 2, Hyperwarp 2, Rincon 5/Arahi 9; notas de clientes BR como camada separada; validação com 30–50 corredores reais.

## Rodada 1: calibração inicial (32 tênis)
- 165 reviews lidas. Concordância com o consenso subiu em todos os índices (amortecimento 0,55→0,88; resposta 0,62→0,97; leveza 0,86→0,99; estabilidade 0,64→0,98; durabilidade 0,30→0,81).
- Correções de dados: maciez, pesos de supertênis, drops medidos (Cumulus 28 13 mm, Kayano 32 8 mm), durabilidade, forma larga, categorias e preços.
- Motor: etiquetas de usos indicados, "não indicado para" e perfil ideal; Fit Score com bônus/penalidades por etiqueta e aprovação ponderada; supertênis entra para maratona e meia competitivas (nível ≥3, treino de ritmo e orçamento ≥ R$ 1.000).
- Perguntas: removida "Tem prova marcada?" (0% de influência); adicionadas pisada, calor, uso fora da corrida e dor no tendão de Aquiles.
