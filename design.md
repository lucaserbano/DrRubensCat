# Design — Site Dr. Rubens Cat

*Guia de aplicação da identidade visual no site. Traduz o manual de marca para decisões concretas de web.*

Fonte original: `id-visual/manual-de-marca/Dr. Rubens Cat - Marca.pdf` e `Dr. Rubens Cat - Identidade Visual.pdf`.

---

## Princípios de design

A identidade no site deve transmitir **confiança médica, cuidado profundo e acolhimento humano**, sem cair em estética hospitalar nem em infantilização literal. O caminho é **sofisticação discreta**.

| Faça | Evite |
|---|---|
| Cores dessaturadas, paleta restrita | Cores vibrantes, gradientes saturados |
| Formas suaves, cantos arredondados moderados | Cantos vivos agressivos ou bordas grossas |
| Espaço em branco generoso | Layouts densos, blocos colados |
| Ilustrações da marca usadas com parcimônia | Múltiplos personagens na mesma tela |
| Tipografia clara, hierarquia firme | Mistura de fontes externas |
| Linguagem que orienta e acompanha | Alarmismo, urgência promocional, jargão técnico |

A metáfora oceânica é tom, não tema. Não usar peixes, corais ou ondas literais como decoração — só os elementos abstratos da marca e os 3 personagens oficiais.

---

## Paleta de cores

### Cores oficiais

| Token | Nome | HEX | Papel no site |
|---|---|---|---|
| `--profundeza` | Profundeza | `#232429` | Texto principal, cabeçalhos sobre fundos claros, fundos escuros de seção dramática |
| `--mar-aberto` | Mar Aberto | `#3C608A` | **Cor primária de marca.** Botões, links, destaques, headings de seção, ícones |
| `--nevoa` | Névoa | `#90A0B5` | Texto secundário, ícones inativos, bordas, dividers, estados disabled |
| `--abrigo` | Abrigo | `#BFC9B9` | Fundos de seção alternativos, cards calmos, destaques sutis |
| `--branco` | Branco | `#FFFFFF` | Fundo padrão, texto sobre fundos escuros |

### Papéis em UI

| Função | Cor | Observação |
|---|---|---|
| Fundo padrão da página | `#FFFFFF` | |
| Texto corrido | `#232429` | Nunca preto puro `#000` |
| Texto secundário / legendas | `#90A0B5` | Suaviza informação de apoio |
| Link / CTA primário | `#3C608A` | |
| Hover de link | `#232429` | Escurece em vez de mudar de matiz |
| Botão primário (fundo) | `#3C608A` | Texto branco |
| Botão primário (hover) | `#2E4D70` *(escurecimento de Mar Aberto, ~20%)* | |
| Botão secundário | Borda `#3C608A` · texto `#3C608A` · fundo transparente | |
| Fundo de seção alternada | `#BFC9B9` ou `#F5F5F0` *(tint sutil)* | Quebrar monotonia entre seções |
| Fundo escuro (hero opcional) | `#232429` | Texto branco; usar com moderação |
| Bordas e dividers | `#90A0B5` em opacidade reduzida (20–30%) | |
| Estados de erro / atenção | Não usar vermelho saturado. Usar Profundeza + ícone | A marca não é alarmista |

### Regras de combinação

- **Contraste mínimo:** texto sobre fundo precisa atingir AA (4.5:1). Profundeza sobre Branco e Branco sobre Mar Aberto passam. Profundeza sobre Abrigo passa. **Mar Aberto sobre Abrigo não passa para texto pequeno** — usar só em elementos grandes ou ilustrativos.
- **Nunca colocar Névoa sobre Branco para texto** — contraste insuficiente.
- **No máximo 3 cores da paleta por tela**, fora preto/branco. Excesso quebra a sensação de calma.
- Hierarquia padrão: Branco (fundo) → Profundeza (texto) → Mar Aberto (acentos) → Abrigo (seções de destaque).

---

## Tipografia

### Família única: Bricolage Grotesque

Toda a tipografia textual usa **Bricolage Grotesque**, presente em `id-visual/fonte-Bricolage-Grotesque/`. Carregar via `@font-face` com os arquivos `.ttf` locais.

Pesos a carregar para o site (subset suficiente):
- Light (300)
- Regular (400)
- Medium (500)
- SemiBold (600)
- Bold (700)
- ExtraBold (800)

> **Nota sobre o wordmark "Dr. Rubens Cat":** o serif do logotipo NÃO é Bricolage. Não tentar recriar via CSS — sempre usar os SVGs da pasta `marca-primaria/` ou `marca-secundaria/`.

### Escala tipográfica

| Token | Tamanho (desktop) | Mobile | Peso | Line-height | Uso |
|---|---|---|---|---|---|
| `--text-display` | 64px | 40px | 700 (Bold) | 1.05 | Hero headline |
| `--text-h1` | 48px | 32px | 700 | 1.1 | Título de página |
| `--text-h2` | 36px | 28px | 600 | 1.15 | Título de seção |
| `--text-h3` | 24px | 22px | 600 | 1.25 | Subtítulo |
| `--text-h4` | 20px | 18px | 500 | 1.3 | Cabeçalho de card |
| `--text-body-lg` | 20px | 18px | 400 | 1.55 | Lead / parágrafo de abertura |
| `--text-body` | 17px | 16px | 400 | 1.6 | Texto corrido |
| `--text-small` | 14px | 14px | 400 | 1.5 | Legendas, metadados |
| `--text-micro` | 12px | 12px | 500 | 1.4 | Labels, tags |

### Regras de uso

- **Sem itálico** em hierarquia principal — só em citações e ênfases pontuais
- **Sem caixa-alta** em parágrafos. Permitida em labels micro (ex: "PEDIATRIA", "BLOG", botões pequenos) com letter-spacing de 0.05–0.1em
- Comprimento de linha de leitura: **65–75 caracteres** (max-width ~70ch)
- Espaço entre parágrafos: 1em mínimo
- **Drop dos pesos finos (200, 300) para corpo de texto pequeno** — perdem legibilidade em telas
- Headings usam Bold ou SemiBold; corpo, Regular

### Padrão de ênfase em headings

Inspirado nas peças do manual ("Pediatria com **presença, atenção e cuidado**"):

- Headings podem ter parte do texto em `--mar-aberto` para criar ritmo visual
- Aplicar em palavras-chave do conceito da marca, não em palavras funcionais
- Usar com moderação: 1 heading com ênfase de cor por seção

---

## Logo / Marca

### Hierarquia de uso no site

| Local | Símbolo | Versão | Pasta |
|---|---|---|---|
| **Navbar (todas as páginas)** | Explorador | Marca primária, fundo claro | `id-visual/marca-primaria/` |
| **Footer** | Explorador | Marca primária, monocromática se sobre Mar Aberto/Profundeza | `id-visual/marca-primaria/` |
| **Hero principal (Início)** | Explorador | Marca primária | `id-visual/marca-primaria/` |
| **Seção Pré-natal** | Guardiã (baleia) | Marca secundária | `id-visual/marca-secundaria/DrRubensCat_guardia_*.svg` |
| **Página/seção "Quando ir ao PA"** *(em Meus artigos)* | Elmo Protetor | Marca secundária | `id-visual/marca-secundaria/DrRubensCat_elmo_*.svg` |
| **Favicon e ícones de app** | Apenas o símbolo Explorador isolado | `ilustracoes-svg/Explorador_*.svg` | |

O Explorador é o símbolo prioritário e a marca padrão. Guardiã e Elmo entram pontualmente para criar variação narrativa em seções com tom específico (proteção / orientação).

### Versões disponíveis

- **Marca primária** (`marca-primaria/`): 6 variações do Explorador + wordmark
- **Marca secundária** (`marca-secundaria/`): 3 variações com Guardiã + 3 com Elmo
- Sempre escolher a versão pelo fundo: clara sobre escuro, escura sobre claro, monocromática sobre cores da paleta

### Regras de uso

- **Sempre usar o SVG.** Nunca recriar o wordmark em CSS, nunca rasterizar para tamanhos abaixo de 200px de largura
- **Tamanho mínimo de aplicação:** 120px de largura para a assinatura completa; 32px para o símbolo isolado
- **Área de proteção** (do manual):
  - Explorador: 1x à esquerda, 2x acima do logotipo (medida = altura da letra "D")
  - Guardiã: 1x à esquerda, 2x acima
  - Elmo: 0,8x à esquerda
  - Nunca colocar texto, ícone ou outro elemento dentro dessa área

### O que não fazer com a marca

- Esticar, distorcer, rotacionar
- Aplicar sombra, brilho, gradiente
- Trocar a cor para fora da paleta oficial
- Separar símbolo e logotipo na mesma tela (exceto navbar mobile, onde o símbolo isolado é aceitável)
- Colocar sobre fundos com baixo contraste ou imagens visualmente carregadas

---

## Elementos decorativos

### Elementos abstratos (`elementos-svg/`)

13 elementos orgânicos disponíveis: ondas, zigue-zague, pontos, raios, arco, círculo, setas, cubo, traços diagonais, sol estilizado.

**Papel no site:**
- Acentos visuais entre seções
- Detalhes em cards (canto, divisor)
- Marcação de listas ou bullets
- Pontuação de transições

**Regras:**
- **Máximo 1–2 elementos por viewport** — eles existem para criar respiração, não para preencher
- Aplicar nas cores da paleta, nunca em cores externas
- Tamanho discreto: raramente passam de 80–120px no desktop
- Nunca usar como background tiled (perde o gesto manual)
- Espaçar dos elementos textuais — eles funcionam como pausa, não como ornamento

### Ilustrações dos personagens (`ilustracoes-svg/`)

5 variações de cada um: Explorador, Guardiã, Elmo Protetor.

**Quando usar:**
- Seções vazias / empty states
- Cabeçalhos de seção temática
- 404 e páginas de erro
- Cards de destaque pontuais

**Quando NÃO usar:**
- Repetição da mesma ilustração na mesma tela
- Mais de um personagem na mesma seção
- Como decoração de fundo atrás de texto crítico

### Imagens fotográficas

Quando o site usar fotos:
- **Cenas reais com famílias** — naturais, sem pose de banco de imagem
- **Tons compatíveis** com a paleta (azuis, beges, neutros)
- **Crianças sorrindo de forma genuína**, não em close clínico
- Evitar fotos de consultório clínico estéril, jaleco isolado, estetoscópio em close
- Foto profissional do Dr. Rubens deve ser usada com tratamento que preserve calma (sem alta saturação ou luz dura)

---

## Aplicações de uso (componentes web)

### Botões

| Tipo | Estilo |
|---|---|
| **Primário** | Fundo `--mar-aberto`, texto branco, padding 14px 28px, border-radius 8px, peso 600. Hover: escurecer fundo ~15% |
| **Secundário** | Borda 1.5px `--mar-aberto`, texto `--mar-aberto`, fundo transparente. Hover: fundo `--mar-aberto` 8% opacity |
| **Terciário (link)** | Texto `--mar-aberto`, sublinhado em hover apenas |
| **CTA navbar** | Variação compacta do primário, padding 10px 20px |

Sem `text-transform: uppercase` em botões grandes. Em botões micro (tags, filtros), maiúscula com letter-spacing aceitável.

### Cards

- Fundo `#FFFFFF` ou `--abrigo` em opacidade leve
- Borda opcional 1px `--nevoa` em 20% opacidade
- Border-radius 12–16px (forma suave, não chip)
- Sombra muito sutil: `0 2px 12px rgba(35, 36, 41, 0.06)`
- Padding interno mínimo 24px
- Em hover: levantar com shadow ligeiramente maior, sem mudar cor de fundo

### Seções

- Alternar entre fundo branco e fundo `--abrigo` (ou um tint mais claro do Abrigo) para criar ritmo
- Espaçamento vertical entre seções: 96–120px desktop / 64–80px mobile
- Container max-width sugerido: 1200px com padding lateral 24px

### Hero (página Início)

- Fundo neutro (branco ou Abrigo)
- Headline em Display + ênfase em Mar Aberto
- Subheadline em body-lg
- Botão primário + foto do Dr. Rubens (composição lado a lado em desktop, empilhada em mobile)
- Elemento decorativo discreto como respiro (1 unidade)

### Navbar

- Fundo branco, sticky no topo
- Logo (marca primária Explorador) à esquerda
- Links de navegação ao centro ou à direita, peso 500, cor `--profundeza`
- Botão "Agendar consulta" como CTA primário compacto à direita
- Borda inferior 1px `--nevoa` em 20% opacidade
- Em mobile: hambúrguer + logo + CTA visível

### Footer

- Fundo `--profundeza` ou `--mar-aberto`
- Logo monocromática branca
- Texto em branco e Névoa para hierarquia
- Espaçamento generoso

### Formulários

- Inputs com borda 1px `--nevoa`, border-radius 8px, padding 14px
- Foco: borda `--mar-aberto` 2px, sem outline padrão do navegador
- Labels acima do input em peso 500
- Mensagens de erro em Profundeza com ícone, sem vermelho saturado

### Animações e movimento

- Transições sutis: `200–300ms ease-out`
- Sem animações que chamam atenção (bounce, rotate, parallax dramático)
- Fade-in em scroll é aceitável e recomendado em seções principais
- Hover de imagens: leve scale (1.02) ou aumento de brilho discreto

---

## Acessibilidade

- Todos os textos devem atingir contraste AA mínimo
- Interativos com `:focus-visible` claro (anel `--mar-aberto`)
- Hierarquia semântica de headings respeitada (`<h1>` único por página)
- Imagens com `alt` descritivo; ilustrações decorativas com `alt=""`
- Tamanho de toque mínimo 44x44px em mobile
- Navegação completa via teclado

---

## Estrutura de assets no projeto

```
site/id-visual/
├── manual-de-marca/                       (PDFs de referência — não usar em produção)
├── fonte-Bricolage-Grotesque/             (.ttf — carregar via @font-face)
├── marca-primaria/                        (Explorador + wordmark — 6 versões)
├── marca-secundaria/                      (Guardiã e Elmo + wordmark — 6 versões)
├── ilustracoes-svg/                       (personagens isolados — 5 variações cada)
└── elementos-svg/                         (13 elementos decorativos abstratos)
```

Ao construir o site, copiar os SVGs para `public/` ou `assets/` mantendo a nomenclatura original para rastreabilidade.

---

## Referências

- [estrutura.md](estrutura.md) — arquitetura e copy do site
- [wiki/marca/voz-e-linguagem.md](../wiki/marca/voz-e-linguagem.md) — tom de comunicação
- [wiki/marca/posicionamento.md](../wiki/marca/posicionamento.md) — base estratégica das decisões visuais
