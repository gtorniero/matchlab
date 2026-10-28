# Acessibilidade — WCAG 2.2 AA (out/2026)

Revisão feita em 25/out/2026 no site, na calculadora de litragem e nos três apps (abertura, questionário, prévia e relatório; temas claro e escuro).

## Como testar
- axe-core 4.10 com as regras WCAG 2.0, 2.1 e 2.2 (A e AA) e boas práticas. Meta: zero violações.
- Teclado: Tab do início ao fim, sem perder o anel de foco; Enter e espaço acionam tudo.
- Largura de 320 px e espaçamento de texto aumentado (1.4.10 e 1.4.12) sem rolagem lateral.
- Comparação de tela antes × depois em 1280 e 390 px para garantir que nada muda no layout.
- Antes de lançar: teste com uma pessoa usando NVDA ou VoiceOver.

## Regras para qualquer mudança
- `<html lang="pt-BR">` e um `<main>` por página; um `h1` sempre presente (nos apps, `#a11y-h1` só para leitor de tela fora da abertura) e níveis de título sem pulos.
- Link "Pular para o conteúdo" como primeiro elemento focável.
- Trocou de etapa ou de página: foco no título novo e aviso em região `role="status"`.
- Mensagem de erro com `role="alert"`; resultados que mudam com `aria-live="polite"`, sem repetir a cada movimento de controle.
- Gráfico: `role="img"` com os valores no nome, ou o dado também em texto.
- Conteúdo oculto ou borrado: `aria-hidden` no visual e texto equivalente para leitor de tela.
- Tabela com rolagem: `tabindex="0"`, `role="region"` e nome único.
- 3D ou arrastar: alternativa por teclado (setas); giro automático para com foco, mouse e "reduzir movimento".
- Contraste mínimo de 4,5:1 para texto (3:1 para texto grande e ícones). Laranja do Tenis sobre azul-petróleo: usar #FFA366.
- Área de toque de pelo menos 24 × 24 px (pode ser invisível com `::after`); links dentro de frase são exceção.
- Imagem de relatório: descrição completa com produto, nota e principais medidas.

## Estado
| Página | axe (violações) | Teclado | 320 px |
|---|---|---|---|
| Home, páginas dos apps, Blog, artigo | 0 | ok | ok |
| Calculadora de litragem | 0 | ok | ok |
| Racket, Board e Tenis Match (4 etapas, 2 temas) | 0 | ok | ok |
