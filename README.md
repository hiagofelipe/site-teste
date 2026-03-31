# ConectaSoft Automações — Site Institucional

Site institucional da **ConectaSoft Automações**, empresa especializada em soluções de automação inteligente para ambientes urbanos e rurais em todo o Brasil.

---

## Sobre o projeto

Single-page em HTML puro com CSS e JavaScript embutidos — sem dependências externas, sem frameworks. Toda a experiência é entregue em um único arquivo `index.html` + `especialista.jpg`.

**Stack:**
- HTML5 semântico
- CSS3 com variáveis customizadas, Grid, Flexbox, animações e `backdrop-filter`
- JavaScript vanilla com `IntersectionObserver` e `requestAnimationFrame`
- Google Fonts: Exo 2 (títulos) + Mulish (corpo)

---

## Estrutura do site

| Seção | ID | Descrição |
|---|---|---|
| Navegação | `#navbar` | Barra fixa com scroll blur, menu mobile animado |
| Hero | `#hero` | Headline, CTAs, painel visual animado, indicador de scroll |
| Sobre a empresa | `#inicio` | Proposta de valor e diferenciais em checklist |
| Especialista | `#especialista` | Perfil do Felipe com foto e animações de arcos |
| Serviços | `#servicos` | 6 cards: Iluminação, Câmeras, Alimentação Animal, Rural, Acesso, Personalizados |
| Diferenciais | `#diferenciais` | 24h, 100% Personalizado, Fácil, Rápido, Garantia |
| Ambientes | `#ambientes` | Urbano vs Rural com chips descritivos |
| CTA Final | `#cta-final` | Box de conversão com botão WhatsApp |
| Rodapé | `footer` | Links, redes sociais, copyright |

---

## Paleta de cores

| Variável | Valor | Uso |
|---|---|---|
| `--blue-deep` | `#050f1e` | Fundo principal |
| `--blue-main` | `#1565c0` | Azul primário (botões, acentos) |
| `--blue-light` | `#42a5f5` | Azul claro (links, bordas hover) |
| `--accent-cyan` | `#00e5ff` | Destaque tecnológico |
| `--green-main` | `#2e7d32` | Verde primário (rural, sustentável) |
| `--green-light` | `#66bb6a` | Verde claro (chips, ícones) |
| `--accent-lime` | `#76ff03` | Acento vibrante em gradientes |

---

## Melhorias implementadas (v2)

### Correções de bugs
- Seletor CSS `#sobre::before` corrigido para `#inicio::before` (ID inexistente)
- Elementos `#scrollProgress` e `#backToTop` existiam no CSS mas não no HTML — adicionados
- JavaScript para scroll progress bar e botão back-to-top implementados (estavam ausentes)
- Links externos agora incluem `rel="noopener noreferrer"` (segurança)

### Novas funcionalidades
- **Barra de progresso de leitura** — mostra o avanço na página em tempo real
- **Botão "voltar ao topo"** — aparece após 400px de scroll com animação suave
- **Animação de contagem** nos stats da hero (500+, 10+) via `IntersectionObserver`
- **Indicador de scroll** no hero (chevron animado "Explorar")
- **Active link** no menu de navegação com underline gradiente dinâmico
- **Scroll handler otimizado** com `requestAnimationFrame` para evitar layout thrashing

### Aprimoramentos visuais
- Cards de serviços: borda superior colorida sempre visível (sutil), intensifica no hover
- Cards de diferenciais: linha gradiente inferior aparece no hover
- Ambiente cards: `translateY` no hover em vez de `scale` — movimento mais elegante
- Botão WhatsApp recebe o mesmo efeito shimmer dos demais botões
- Ícones dos cards de serviços com destaque de borda e fundo no hover
- Mobile nav: animação `slideIn` ao abrir, ícones nos itens, fecha ao clicar fora
- `aria-expanded` atualizado dinamicamente no hamburger (acessibilidade)
- `aria-label` e `aria-hidden` adicionados nos elementos interativos e SVGs decorativos
- `loading="lazy"` na foto do especialista
- Scroll events com `{ passive: true }` para melhor performance em mobile

### Organização do código
- Inline styles do `#cta-final` movidos para CSS
- Todos os `@keyframes` agrupados em bloco único no início do CSS
- Espaçamento de seções padronizado em `116px` (era inconsistente)
- Container com `padding: 0 28px` para melhor respiro lateral

---

## Como usar

Basta abrir o `index.html` em qualquer navegador moderno. Nenhum servidor ou build necessário.

Para atualizar a foto do especialista, substitua `especialista.jpg` na raiz do projeto mantendo o mesmo nome.

---

## Contato / Conversão

Todos os CTAs direcionam para WhatsApp:
```
https://wa.me/5561985682000
```
Mensagem pré-preenchida: _"Olá, Felipe! Vim pelo site e gostaria de mais informações sobre os serviços de automações."_

---

© 2026 ConectaSoft Automações. Todos os direitos reservados.
