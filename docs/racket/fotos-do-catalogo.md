# Racket Match — fotos do catálogo (out/2026)

Objetivo: foto de produto das 58 raquetes, com direito de uso claro. Enquanto uma raquete não tiver foto autorizada, o app segue com a silhueta geométrica.

Regra: nada de copiar foto de loja ou de site de marca sem autorização. Foto não muda ranking; afiliado só depois da recomendação e declarado.

## Caminho 1 — autorização das marcas

### Quem pedir (9 marcas, 58 raquetes)

| Marca | Nº | Modelos | Contato | Status |
|---|---|---|---|---|
| Head | 14 | Speed MP, Speed MP L, Speed Pro, Speed Team, Gravity MP, Gravity Pro, Boom MP, Boom Team, Radical MP, Extreme MP, Extreme Team, Prestige MP, Instinct MP, Ti S6 | | |
| Wilson | 11 | Blade 98 16x19 v9, Blade 100L v9, Blade 104 v9, Clash 100 v3, Clash 100L v3, Clash 108 v3, Ultra 100 v5, Ultra 100L v5, Pro Staff 97 v14, Shift 99 v1 300 g, Burn 100 v5 | | |
| Babolat | 10 | Pure Aero 98, Pure Aero, Pure Aero Team, Pure Aero Lite, Pure Drive, Pure Drive Team, Pure Drive Lite, Pure Strike 100 16x19, Pure Strike 98 16x19, Boost Drive | | |
| Yonex | 8 | EZONE 98, EZONE 100, EZONE 100L, VCORE 98, VCORE 100, VCORE 100L (8ª geração), Percept 97, Percept 100 | | |
| Dunlop | 4 | CX 200, CX 200 Tour 16x19, SX 300, FX 500 | | |
| ProKennex | 3 | Ki Q+ Tour 300 g, Black Ace 300, Black Ace 105 | | |
| Volkl | 3 | Vostra V1 Pro, Vostra V1 MP, Vostra V8 300 g | | |
| Prince | 3 | Phantom 100X 290 g, Tour 100 290 g, Ripstick 100 300 g | | |
| Tecnifibre | 2 | TF40 305 16x19, TFight 300 | | |

Não achamos por busca o distribuidor oficial de cada marca no Brasil. Onde procurar o contato, nesta ordem:
1. Perfil oficial da marca no Brasil no Instagram (DM ou e-mail na bio): costuma ser o distribuidor.
2. Formulário de contato ou "press/media" do site global da marca.
3. LinkedIn: gerente de marketing da marca no Brasil ou na América Latina.

Prazo sugerido: cobrar uma vez depois de 10 dias úteis.

### E-mail (português)

**Assunto:** Pedido de uso de fotos de produto: Racket Match (comparador independente de raquetes)

Olá, equipe [MARCA],

Sou [NOME], da Beyond the Work. Mantemos o Racket Match (matchlab…/apps/racket), um teste gratuito em português que indica a raquete de tênis mais adequada ao jogo de cada pessoa, a partir de cerca de 30 perguntas e das especificações medidas de 58 raquetes de 9 marcas.

Hoje mostramos as raquetes como desenho técnico. Gostaríamos de exibir a foto oficial dos modelos [MARCA] que estão no catálogo:

[LISTA DE MODELOS]

Como usaríamos as imagens:
- só a foto do produto, ao lado da ficha técnica e do resultado do teste;
- sem alteração, com crédito "Imagem: [MARCA]";
- sem uso em anúncio e sem sugerir patrocínio ou parceria.

O ranking é independente: nenhuma marca paga para aparecer, e a foto não muda a recomendação. Se houver link de compra no futuro, ele aparece só depois do resultado e é declarado.

Vocês poderiam autorizar o uso e indicar onde baixar as imagens (banco de imagens, kit de imprensa ou arquivos)? Fundo branco, 1000 px ou mais, é o ideal. Se houver termos de uso, seguimos à risca.

Obrigado,
[NOME] · Beyond the Work · [E-MAIL] · [TELEFONE]

### E-mail (inglês, para matriz)

**Subject:** Product image permission request: Racket Match (independent racquet finder, Brazil)

Hi [BRAND] team,

I'm [NAME] from Beyond the Work. We run Racket Match, a free Portuguese-language quiz that matches Brazilian players to a tennis racquet using about 30 questions and measured specs for 58 racquets from 9 brands.

We currently show racquets as technical drawings and would like to display official product photos of these [BRAND] models:

[MODEL LIST]

How we'd use them: product photo only, next to the spec sheet and quiz result; unaltered, credited "Image: [BRAND]"; no advertising use, no implied sponsorship.

Rankings are independent: no brand pays to appear, and images don't affect recommendations. Any future purchase link appears only after the result and is disclosed.

Could you grant permission and point us to a media library or press kit? White background, 1000 px or larger, is ideal. We'll follow any usage terms you have.

Thanks,
[NAME] · Beyond the Work · [EMAIL]

## Caminho 2 — feed de afiliado

Imagem vinda do feed de afiliado da loja, exibida com o link do produto. Serve também para o link de compra que entra depois do pagamento real.

| Rede / loja | O que se sabe | Atenção |
|---|---|---|
| **Centauro (Awin)** | Vende raquetes Babolat e Yonex no Brasil | Termos da Awin: não aceita afiliado pessoa física (precisa CNPJ); cookie de 1 dia; sem remarketing nem popup em produto e carrinho |
| **Netshoes (Awin)** | Programa na Awin, comissão progressiva | Cadastro exige conta Awin; conferir se o feed traz raquetes |
| **ArtWalk (Awin)** | Especialista em calçado de tênis | Útil para o Tenis Match, não para raquete |
| **Amazon (Creators API)** | Substituiu a API antiga | Exige conta de afiliado com vendas; imagem exibida dos servidores da Amazon, sem baixar |
| **Tennis Warehouse** | Base mais completa | Novos afiliados pausados; exige exclusividade de varejo de tênis |
| **Mercado Livre** | API com token | Fotos dos vendedores, qualidade irregular |

### Passos
1. Criar conta de publisher na Awin com o CNPJ da Beyond the Work.
2. Pedir entrada nos programas Centauro e Netshoes, citando o Racket Match e o modelo "link só depois da recomendação, declarado".
3. Aprovado, baixar o feed de produtos e casar cada raquete do catálogo pelo nome do modelo e geração. Conferir à mão: lojas misturam gerações e versões (L, Team, Lite).
4. Guardar no catálogo só o endereço da imagem e do produto. Respeitar os termos da loja sobre baixar ou não a imagem.
5. Raquete que nenhum feed cobre continua no caminho 1 ou na silhueta.

## No app (quando houver foto)
- Campo `img` no `CATALOG` com a URL e `imgSrc` com o crédito ("Imagem: Wilson" ou "Imagem: Centauro").
- Sem `img`, fica a silhueta atual. A foto entra na ficha e no relatório; o 3D e a silhueta continuam no comparativo de specs.
- Atualizar `assets/reports/racket.webp` quando a foto aparecer no relatório.
