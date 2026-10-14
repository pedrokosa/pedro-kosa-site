# Site portfólio do Pedro Kosa

Site pessoal de portfólio. Pedro é jornalista com MBA em marketing digital e trabalha com estratégia de conteúdo, redes sociais e ghostwriting para executivos. Público: empresas e gestores no Brasil que contratam conteúdo. O site é a vitrine dele, então o visual faz parte da mensagem.

## Estrutura

- `index.html`: o site inteiro (HTML, CSS e JavaScript num arquivo só). Sem build, sem framework, sem dependências além das fontes do Google Fonts.
- `assets/logos/`: logos das marcas em branco (PNG com transparência).
- `assets/favicon.svg`: favicon provisório.
- `docs/`: contexto do projeto. Leia antes de mudanças grandes.
  - `notas-de-versao.md`: histórico V1 a V9, copy definido pelo Pedro, restrições visuais e pendências. É o documento mais importante.
  - `referencias-visuais.md`: direção de arte e referências.
  - `experiencias.md`: rascunho do currículo, matéria-prima para cases e "Sobre mim".
  - `decisoes-iniciais.md`: por que site próprio, hospedagem, contato, analytics.

## Como o index.html está organizado

- CSS no topo, com tokens de cor em `:root` (`--bg`, `--accent: #FF6A1A`, etc.). Tema único, escuro.
- Fundo: canvas WebGL `#lava` com um shader de lava lamp que reage ao cursor e ao toque. Fallback em CSS (`.lava-fallback`) quando não há WebGL.
- Contato e rodapé ficam num módulo claro (`.light`): uma camada branca com `mix-blend-mode: difference` inverte a lava, que aparece azul ali.
- Conteúdo bilíngue (PT e EN). Os textos ficam em objetos JavaScript no fim do arquivo; `applyLang()` troca o idioma. `#en` no link abre em inglês e a escolha fica salva no navegador.
- Cases: lista de objetos JS que gera os cards e o painel expandido (carrossel, destaque, fatos, prêmio, link). `#case-<id>` no link abre um case direto.
- Marcas: lista de objetos JS com nome, largura relativa e caminho do logo.
- Animações de rolagem em `initReveal()` e `setupCaseMotion()`. Tudo respeita `prefers-reduced-motion`.

## Regras de design (pedidas pelo Pedro, não quebrar)

- Sem chapéus/eyebrows acima dos títulos, sem letras espaçadas (tracking largo), sem linhas decorativas, sem ícones pequenos arredondados com bolinha e borda fina de acento, sem outros maneirismos típicos de site feito por IA.
- Movimento só quando ajuda a hierarquia ou a leitura, nunca como enfeite. Cada animação de entrada acontece uma vez.
- Tipos: Schibsted Grotesk (títulos e interface) e Newsreader (texto corrido).
- Laranja `#FF6A1A` é o único acento.
- Cases em cards enxutos, um resultado por card. Nada de prints gigantes.
- Referências são para extrair princípios, nunca copiar layouts.

## Regras de texto

- Copy em português do Brasil, tom neutro puxando para o casual: pragmático e pessoal, sem ser engraçadinho.
- O Pedro evita travessão (em dash), emoji e negrito nos textos dele. Não introduza isso no copy do site.
- Textos já definidos pelo Pedro (hero, abertura, nomes dos serviços) estão em `docs/notas-de-versao.md`. Não reescreva sem ele pedir.
- Ao mexer num texto em português, atualize também a versão em inglês (ou avise que ficou pendente).
- Marcadores `[NÚMERO]`, `[PRAZO]`, `[VEÍCULOS]` nos cases são lacunas que o Pedro vai preencher. Não invente números.

## Como trabalhar

- Para ver o site: `python3 -m http.server 8000` na pasta e abrir http://localhost:8000.
- Teste sempre em largura de celular (cerca de 390 px), tablet e desktop. Os cases têm comportamento diferente em 1 coluna (empilhados) e em 2 ou 4 colunas (distribuídos como cartas).
- Teste com "reduzir movimento" ligado.
- Imagens novas: converter para WebP e reduzir antes de colocar em `assets/`.
- Mudanças pequenas e verificáveis. Antes de reestruturar o arquivo (por exemplo, separar CSS e JS), pergunte.
- Se o projeto estiver num repositório git, faça um commit por mudança, com mensagem em português.

## Contato real (já no site)

WhatsApp: wa.me/5511984300902 (com mensagem pré-preenchida). E-mail: pedrokosa@gmail.com. LinkedIn, Instagram e TikTok: pedrokosa.

## Pendências principais

Ver lista completa em `docs/notas-de-versao.md`. As que dependem de código: Open Graph com domínio real e imagem `assets/og-image.png` (1200x630); sitemap.xml e robots.txt quando o domínio existir; arquivo `CNAME` para o GitHub Pages; GA4 ou Cloudflare Web Analytics (com aviso de privacidade se usar cookies); favicon definitivo; fotos dos cases e do "Sobre mim".
