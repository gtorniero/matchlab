# MATCH LAB

Site guarda-chuva com três testes de equipamento: Racket Match (raquete de tênis), Board Match (prancha de surf) e Tenis Match (tênis de corrida). Projeto da Beyond the Work. Tudo é HTML, CSS e JS estático, sem build.

## Estrutura

| Pasta | O que é | Quem mexe |
| --- | --- | --- |
| `index.html` | Home, páginas de cada app, biblioteca e leitor de artigos (roteamento por `#hash`) | Sessão do site |
| `content/` | Os 45 artigos (`raquete.js`, `tenis.js`, `prancha.js`), formato em `docs/guia-de-artigos.md` | Sessão do site |
| `assets/reports/` | Imagens dos relatórios de exemplo usadas na home e nas páginas dos apps | Sessão do site |
| `apps/racket/` | Racket Match, arquivo único `index.html` | Sessão do Racket |
| `apps/board/` | Board Match, arquivo único `index.html` | Sessão do Board |
| `apps/tenis/` | Tenis Match, arquivo único `index.html` | Sessão do Tenis |
| `docs/` | Contexto: padrão do relatório PDF, teste de fogo e, em `docs/<app>/`, benchmark, catálogo e calibração de cada app | Cada sessão atualiza o seu |

Leia `docs/padrao-relatorio-pdf.md` e a pasta `docs/<app>/` do seu app antes de mexer no motor ou no relatório. Registre ali as rodadas novas de calibração.

## Regras

- Cada sessão mexe só na sua pasta. Mudança fora dela vira pull request separado e com explicação.
- Trabalhe numa branch e abra pull request; nada vai direto para `main`.
- Cada app mantém no header o link `← MATCH LAB` apontando para `../../`.
- Quando um app mudar o relatório de forma visível, atualize a imagem em `assets/reports/<app>.webp` (captura do relatório do "Ver um exemplo pronto", 1000 px de largura).
- Quando mudar número de perguntas, tamanho de catálogo ou preço de um app, atualize os `facts` desse app em `index.html` no mesmo pull request.
- Identidade: marca-mãe MATCH LAB em preto e sóbria; cor só nos apps (Racket #DDF247, Board #6CCFF6, Tenis #FF8A3D, base azul-petróleo #0E4D64). Títulos em Archivo, texto em DM Sans, logos em Syne. Footer com assinatura "Um projeto Beyond the Work".
- Textos em português do Brasil, diretos, sem jargão. Nenhuma marca paga para aparecer no resultado; afiliado só depois da recomendação e declarado.
- Pagamento ainda é simulado. Especificações de catálogo são aproximadas até a revisão por professores.

## Testar

`python3 -m http.server` na raiz e abra `http://localhost:8000`.
