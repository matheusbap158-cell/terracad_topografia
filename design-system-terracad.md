# Design System - TerraCad Topografia & Geoprocessamento

Base extraída da logo real (um "T" estilizado em verde e branco sobre azul-petróleo, arquivo de 150 px) e das fotos de campo (equipamentos amarelos, canteiros de obra). Público B2B: construtoras, engenheiros, loteadores e indústrias.

## Resumo do tom visual
- Azul-petróleo profundo da logo como base, com muito branco e cinza-azulado: técnico e confiável.
- Âmbar (amarelo de sinalização) só nos botões e destaques, ecoando o amarelo dos equipamentos nas fotos.
- Linhas de curva de nível, malha de coordenadas, miras e numeração de estaca ("0+000") como ornamento, sem poluir.

## 1. Cores

| Token | Hex | Uso |
|---|---|---|
| --ink-950 | #06202A | Fundo do hero, rodapé, blocos escuros |
| --ink-900 | #0A2B38 | Seção escura alternada |
| --ink-800 | #0F3A4B | Cards sobre fundo escuro |
| --teal-600 | #1A6482 | Cor da marca (logo); títulos e links sobre fundo claro |
| --teal-500 | #147193 | Fundo da logo; destaques secundários |
| --green-400 | #2FB38E | Verde da logo; pequenos detalhes e ícones (nunca em botão) |
| --amber-400 | #F5B82E | Cor de ação: botão primário e destaque em fundo escuro |
| --amber-500 | #E5A112 | Hover do botão primário |
| --paper-50 | #F4F7F8 | Fundo claro padrão |
| --paper-100 | #E6EDF0 | Seção clara alternada |
| --line | #C9D6DB | Bordas e divisores em fundo claro |
| --text | #0B2530 | Texto principal em fundo claro |
| --muted | #4C6470 | Texto secundário em fundo claro |
| --text-on-dark | #E8F1F4 | Texto principal em fundo escuro |
| --muted-on-dark | #9DB6C0 | Texto secundário em fundo escuro |
| --wa-500 | #25D366 | EXCLUSIVO do botão flutuante de WhatsApp |

Contrastes: #E8F1F4 sobre #06202A acima de 14:1; #9DB6C0 sobre #0A2B38 acima de 6:1; #06202A sobre #F5B82E acima de 10:1; #4C6470 sobre #F4F7F8 acima de 5:1.

## 2. Tipografia (Google Fonts)
- Títulos: Archivo (700 e 800), firme e técnica.
- Corpo: Inter (400, 500, 600).
- Números e rótulos técnicos: IBM Plex Mono (500).

| Nível | Desktop | Mobile | Peso | Entrelinha | Espaçamento |
|---|---|---|---|---|---|
| H1 | 72px | 42px | 800 | 1.02 | -0.025em |
| H2 | 44px | 31px | 800 | 1.08 | -0.02em |
| H3 | 21px | 20px | 700 | 1.25 | -0.01em |
| Rótulo (mono) | 12.5px | 12px | 500 | 1.4 | 0.14em, maiúsculas |
| Corpo | 17px | 16px | 400 | 1.7 | 0 |
| Botão | 15px | 15px | 700 | 1 | 0.02em |

## 3. Componentes
- **Botão primário:** fundo âmbar (#F5B82E), texto #06202A, raio 10px, altura mínima 54px. Hover: #E5A112 e sobe 2px. Foco: contorno branco de 3px com afastamento.
- **Botão secundário:** transparente com borda de 1px (branca a 40% no escuro, #1A6482 no claro).
- **Card claro:** branco, borda 1px #C9D6DB, raio 14px, número de estaca em mono no canto.
- **Card escuro:** #0F3A4B, borda 1px branca a 12%, raio 14px.
- **Input e select:** altura 52px, raio 10px, borda #C9D6DB. Foco: borda #1A6482 e contorno visível. Erro: borda #B3492E com texto de ajuda.

## 4. Estética
- Raios: 10px (campos e botões), 14px (cards). Aparência mais "reta" que arredondada, para passar rigor.
- Sombras: suaves e curtas (0 10px 30px rgba(6,32,42,.12)) só em cards claros.
- Espaçamento: escala de 8px (8, 16, 24, 32, 48, 72, 104). Seções com 104px no desktop e 64px no mobile.
- Ornamentos: curvas de nível em SVG (opacidade 6 a 10%), malha de coordenadas, miras nos cantos das fotos e rótulos tipo "EST. 0+240".

## 5. Conversão
- Botão âmbar "Solicitar orçamento" no topo, após os serviços, no case, nos passos e no fim.
- Formulário de orçamento que abre o WhatsApp com a mensagem pronta (serviço, tipo de projeto, cidade).
- Prova real: fotos de campo, a obra do shopping e a nota 5,0 do Google.
- Verde do WhatsApp só no botão flutuante.

## Tokens prontos (CSS)
```css
:root{
  --ink-950:#06202A; --ink-900:#0A2B38; --ink-800:#0F3A4B;
  --teal-600:#1A6482; --teal-500:#147193; --green-400:#2FB38E;
  --amber-400:#F5B82E; --amber-500:#E5A112;
  --paper-50:#F4F7F8; --paper-100:#E6EDF0; --line:#C9D6DB;
  --text:#0B2530; --muted:#4C6470;
  --text-on-dark:#E8F1F4; --muted-on-dark:#9DB6C0;
  --wa-500:#25D366; --alert-600:#B3492E;
  --font-display:'Archivo',system-ui,sans-serif;
  --font-body:'Inter',-apple-system,'Segoe UI',sans-serif;
  --font-mono:'IBM Plex Mono',ui-monospace,monospace;
  --r-ctl:10px; --r-card:14px;
}
```
