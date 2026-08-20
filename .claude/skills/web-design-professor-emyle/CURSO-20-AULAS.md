# Curso — 20 Aulas de Web Design e Front-end (Emyle)

Currículo prático da skill web-design-professor-emyle. Cada aula segue o mesmo formato: conceito, quando usar, quando não usar, e exercício aplicado em cima de um projeto real.

## Como usar este curso

Comandos: "começar aula 1", "continuar meu curso", "qual aula estou?", "revisar aula N", "fazer exercício da aula N".

O progresso é conversacional. Registre em qual aula a Emyle parou para retomar sem repetir do zero.

## Aula 1 — Como uma página web é estruturada

CONCEITO: uma página é uma árvore de caixas (div, section, header). O navegador empilha essas caixas de cima para baixo por padrão, e o CSS diz "não empilha assim, organiza deste outro jeito".

QUANDO USAR: é a base de tudo. HTML define conteúdo e ordem, CSS define aparência e layout, JS define comportamento.

QUANDO NÃO USAR: tentar resolver com CSS um problema que na verdade é de ordem do HTML.

EXERCÍCIO: escolha uma seção do site e liste a árvore de caixas dela.

## Aula 2 — Viewport, section e container

CONCEITO: viewport é o que a pessoa vê; section normalmente ocupa 100% da largura; container é um limite interno que centraliza o conteúdo dentro da section.

QUANDO USAR: sempre que a seção precisar de fundo esticando até a borda, mas o texto precisar ficar recuado e legível.

QUANDO NÃO USAR: não coloque max-width na section inteira, isso corta o background. Limite o container interno.

EXERCÍCIO: confirme se cada section tem container interno, ou se o texto estica a tela toda em monitores grandes.

## Aula 3 — Centralização e max-width

CONCEITO: margin-inline auto centraliza um elemento com largura definida. width min(1280px, calc(100% - 48px)) cria um container que nunca passa de 1280px nem cola nas bordas.

QUANDO USAR: em praticamente todo container de conteúdo.

QUANDO NÃO USAR: em elementos full-bleed (imagem de fundo, faixa colorida).

EXERCÍCIO: aplique o padrão de container numa seção que hoje está grudada na borda em telas grandes.

## Aula 4 — Flexbox

CONCEITO: flex organiza elementos em linha ou coluna. justify-content controla o eixo principal, align-items controla o eixo cruzado.

QUANDO USAR: menus, cards lado a lado, botões alinhados.

QUANDO NÃO USAR: grids complexos com muitas linhas e colunas ao mesmo tempo.

EXERCÍCIO: no header, use display flex, justify-content space-between e align-items center.

## Aula 5 — Grid

CONCEITO: grid organiza em linhas e colunas ao mesmo tempo. grid-template-columns repeat(3, 1fr) cria 3 colunas iguais, gap controla o espaço.

QUANDO USAR: grade de serviços, cards, portfólio.

QUANDO NÃO USAR: quando só existe uma direção de alinhamento.

EXERCÍCIO: aplique repeat(auto-fit, minmax(240px, 1fr)) na grade de serviços.

## Aula 6 — Espaçamento e alinhamento

CONCEITO: uma escala consistente (4, 8, 12, 16, 24, 32, 48, 64, 80, 96, 128) evita valores aleatórios de padding e margin.

QUANDO USAR: sempre. Antes de escrever margin-top 23px, pergunte se esse valor está na escala.

QUANDO NÃO USAR: única exceção é ajuste fino de 1-2px para correção óptica.

EXERCÍCIO: liste todos os espaçamentos de uma seção e ajuste os que não batem com a escala.

## Aula 7 — Header

CONCEITO: header tem 3 partes (logo, navegação, CTA) e 3 comportamentos: static, sticky e fixed.

QUANDO USAR STICKY: quando o menu precisa estar sempre acessível.

QUANDO NÃO USAR FIXED SEM CUIDADO: fixed tira o elemento do fluxo e sem padding compensatório cobre o topo da página.

EXERCÍCIO: confirme se o header é sticky, tem z-index suficiente, e se o menu mobile abre e fecha sem travar o scroll.

## Aula 8 — Hero

CONCEITO: estrutura clássica é eyebrow, H1, descrição, CTA, prova social. É a seção mais importante.

QUANDO USAR VARIAÇÕES: negócios muito visuais podem deixar a imagem dominar com texto enxuto.

QUANDO NÃO USAR: não encha o hero de texto. Se é difícil resumir em uma frase, o problema é de posicionamento do negócio.

EXERCÍCIO: escreva o H1 do hero em uma frase só.

## Aula 9 — Tipografia

CONCEITO: hierarquia faz o olho saber por onde começar. clamp(2.5rem, 5vw, 4rem) cria um H1 que cresce com a tela sem ultrapassar um limite.

QUANDO USAR CLAMP: em títulos grandes no desktop que não podem quebrar no mobile.

QUANDO NÃO USAR: em textos pequenos, onde tamanho fixo é mais previsível.

EXERCÍCIO: troque um font-size fixo de H1 por clamp e teste em 3 larguras.

## Aula 10 — Cores

CONCEITO: cores como tokens (--primary, --accent, --background) permitem trocar a paleta inteira mudando poucas linhas.

QUANDO USAR: desde o primeiro dia do projeto.

QUANDO NÃO USAR MAIS DE UMA COR DE DESTAQUE: com 4 ou 5 accents tudo grita ao mesmo tempo e a hierarquia se perde.

EXERCÍCIO: liste as cores do site e agrupe em background, foreground, primary, accent, border.

## Aula 11 — Imagens e backgrounds

CONCEITO: img é para conteúdo (precisa de alt); background-image é para decoração. background-size cover e background-position center enquadram sem distorcer.

QUANDO USAR BACKGROUND-POSITION CUSTOMIZADO: quando o assunto da foto não está no centro.

QUANDO NÃO USAR IMAGEM PESADA: um hero não precisa de foto de 8MB. Comprima e use WebP.

EXERCÍCIO: ajuste o background-position até o elemento principal ficar bem enquadrado em mobile e desktop.

## Aula 12 — Frames e cards

CONCEITO: frame é um bloco com border-radius, overflow hidden e aspect-ratio que dá aparência de quadro. Cards são a menor unidade repetível.

QUANDO USAR ASPECT-RATIO: sempre que quiser proporção consistente (16/9, 4/5, 1/1).

QUANDO NÃO USAR RADIUS DIFERENTE EM CADA ELEMENTO: defina 2 ou 3 valores e reuse.

EXERCÍCIO: confira se os cards têm mesma altura, padding e radius entre si.

## Aula 13 — Responsividade

CONCEITO: responsivo não é encolher o desktop, é reconsiderar ordem, tamanho e prioridade. Testar 1440+, 1024-1366, 768, 390, 320-360.

QUANDO USAR BREAKPOINTS: quando o layout visivelmente quebra, não em números arbitrários.

QUANDO NÃO USAR: não crie um breakpoint para cada diferença de pixel.

EXERCÍCIO: redimensione o navegador devagar e anote em qual largura algo quebra.

## Aula 14 — Mobile

CONCEITO: no mobile o menu vira hambúrguer, o hero empilha, e o CTA precisa ser fácil de alcançar com o polegar.

QUANDO USAR 100DVH OU 100SVH: em vez de 100vh, que quebra no mobile por causa da barra de endereço.

QUANDO NÃO USAR: não copie o desktop reduzindo fontes. Repense a ordem das seções.

EXERCÍCIO: abra o site no celular de verdade e veja se algum botão fica difícil de tocar.

## Aula 15 — Scroll e sticky

CONCEITO: position sticky com top definido gruda o elemento dentro do espaço do pai. Diferente de fixed, ele solta quando o pai termina.

QUANDO USAR: texto fixo ao lado de conteúdo que rola, ou o próprio header.

QUANDO NÃO USAR: vários elementos sticky competindo pela mesma área.

EXERCÍCIO: monte uma seção com duas colunas, uma sticky e outra com lista longa rolando ao lado.

## Aula 16 — Reveal, parallax e animação

CONCEITO: reveal é o elemento aparecer suavemente quando entra na tela, via IntersectionObserver. Parallax move elementos em velocidades diferentes no scroll.

QUANDO USAR: reveal sutil melhora o ritmo de leitura; parallax leve adiciona profundidade.

QUANDO NÃO USAR: anime tudo e o efeito cansa. Sempre respeite prefers-reduced-motion.

EXERCÍCIO: aplique reveal simples em 3 elementos e observe o ritmo.

## Aula 17 — Formulários e CTA

CONCEITO: o CTA principal deve ser visível sem rolar muito, repetido em pontos estratégicos, com uma ação clara por vez.

QUANDO USAR MÚLTIPLOS CTAS: quando repetem a mesma ação em pontos diferentes, não quando competem entre si.

QUANDO NÃO USAR FORMULÁRIO LONGO: cada campo extra reduz conversão.

EXERCÍCIO: conte quantos CTAs diferentes existem na Home. Se forem mais de 2 tipos, escolha 1 principal.

## Aula 18 — Performance

CONCEITO: Core Web Vitals medem experiência real. LCP, CLS e INP.

QUANDO USAR LAZY LOADING: em imagens fora da primeira dobra.

QUANDO NÃO USAR: nunca coloque lazy na imagem do hero, ela é o LCP.

EXERCÍCIO: abra o DevTools na aba Network e identifique o maior arquivo carregado.

## Aula 19 — Conversão e UX

CONCEITO: os 4 filtros antes de qualquer decisão vistosa. Design, UX, Performance e Conversão.

QUANDO USAR PROVA SOCIAL: perto do momento de decisão, não isolada numa seção que ninguém lê.

QUANDO NÃO USAR ORIGINALIDADE FORÇADA: o usuário chega com expectativas de outros sites.

EXERCÍCIO: rode o CHECKLIST-REVIEW.md na Home atual e liste os 3 problemas de maior impacto.

## Aula 20 — Projeto final completo

CONCEITO: juntar tudo num projeto do zero, do briefing à auditoria final.

EXERCÍCIO FINAL: escolha um cliente e conduza o workflow completo do SKILL.md, terminando com o CHECKLIST-REVIEW.md.

COMO SABER QUE TERMINOU: a Emyle consegue olhar para qualquer site e explicar por que cada decisão de layout, imagem, espaçamento e movimento foi tomada.
