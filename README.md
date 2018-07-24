<h1 align="center">
<br>
  <img src="https://raw.githubusercontent.com/thedaviddias/Front-End-Performance-Checklist/master/images/logo-front-end-performance-checklist.jpg" alt="Front-End Performance Checklist" width="170">
  <br>
    <br>
  Checklist de Performance Front-End
  <br>
</h1>

<h4 align="center">🎮 O único checklist de performance front-end que roda mais rápido que os outros.</h4>
<p align="center">Apenas uma regra simples: "Faça o design e programe pensando em performance"</p>

<p align="center">
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs são bem vindas">
  </a>
  <a href="https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link">
    <img src="https://img.shields.io/badge/chat-on_gitter-008080.svg?style=flat-square" alt="Gitter">
  </a>
    <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="Licence MIT">
  </a>
</p>

<p align="center">
  <a href="#how-to-use">Como usar</a> • <a href="#contributing">Contribuir</a> • <a href="https://www.producthunt.com/posts/front-end-performance-checklist">Product Hunt</a>
</p>
<p align="center">
    <span>Outros Checklists:</span>
    <br>
  🗂 <a href="https://github.com/thedaviddias/Front-End-Checklist#---------front-end-checklist-">Checklist de Front-End</a> • 💎 <a href="https://github.com/thedaviddias/Front-End-Design-Checklist#front-end-design-checklist">Checklist de Design Front-End</a>
</p>

## Índice

1.  **[HTML](#html)**
2.  **[CSS](#css)**
3.  **[Fontes](#fonts)**
4.  **[Imagens](#images)**
5.  **[JavaScript](#javascript)**
6.  **[Servidor](#server) (em progresso)**
7.  **[Frameworks JS](#js-frameworks) (em progresso)**

## Introdução

Performance é um assunto gigante, mas nem sempre é um assunto de "back-end" ou "admin": também é uma responsabilidade do Front-End. O Checklist de Performance Front-End é uma lista extensa de elementos que você deve conferir ou ao menos estar ciente como um desenvolvedor Front-End e aplicar em seu projeto (pessoal ou profissional).

### Como usar?

Para cada regra, você vai encontrar um parágrafo explicando _por que_ essa regra é importante e _como_ você pode aplicá-la. Para entender melhor, você encontrará links que te direcionarão a 🛠️ ferramentas, 📖 artigos ou 📹️mídias que complementam o checklist.

Todos os itens no **Checklist de Performance Front-End** são essenciais para alcançar o melhor resultado de performance mas você encontrará um indicador para te auxiliar a eventualmente priorizar algumas regras perante outras. Existem 3 níveis de prioridade / impacto:

- ![Baixo][low] significa que o item tem **pouco** impacto e prioridade no seu projeto.
- ![Médio][medium] significa que o item tem **médio** impacto e prioridade no seu projeto. Você não deve evitar resolver esse item.
- ![Alto][high] significa que o item tem **alto** impacto e prioridade no seu projeto. Você não pode evitar seguir a regra e aplicar as correções apropriadas.

### Ferramentas de performance

Lista de ferramentas que você pode usar para testar ou monitorar o seu website ou aplicação:

- 🛠 [WebPagetest - Teste de Performance e Otimização de Websites](https://www.webpagetest.org/)
- 🛠 ☆ [Dareboost: Teste de Velocidade para Website e Análise de Website](https://www.dareboost.com/) (use o cupom WPCDD20 para ter -20%)
- 🛠 [GTmetrix | Otimização de Velocidade e Performance de Website](https://gtmetrix.com/)
- 🛠 [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
- 📖 [Pagespeed - A ferramenta e guia de otimização](https://varvy.com/pagespeed/)
- 📖 [Torne a web mais rápida | Google Developers](https://developers.google.com/speed/)
- 📖 [Sitespeed.io - Bem Vindo ao maravilhoso mundo da Performance da Web](https://www.sitespeed.io/)

### Referências

- 📖 [O Custo do Javascript - YouTube](https://www.youtube.com/watch?v=_bzqF05xsC4) - _(título original: 'The Cost of Javascript', em inglês)_
- 📖 [Entenda a Análise de Performance em Tempo de Execução  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/) - _(título original: 'Get Started With Analyzing Runtime Performance', em inglês)_
- 📖 [A Situação da Web | 2018_01_01](https://httparchive.org/reports/state-of-the-web?start=2018_01_01) - _(título original: 'State of the Web', em inglês)_
- 📖 [O Peso da Página não Importa](https://www.speedshop.co/2015/11/05/page-weight-doesnt-matter.html) - _(título original: 'Page Weight Doesn't Matter', em inglês)_

---

## HTML

![html]

- [ ] **HTML Minificado:** ![medium] O código HTML está minificado, comentários, _white spaces_ e novas linhas são removidas dos arquivos de produção.

  _Por que:_

  > Remover todo o espaço desnecessário, comentarios e quebras reduz o tamanho do seu HTML e acelera o tempo de carregamento do seu site e obviamente reduz o peso do download para o usuário.

  _Como:_

  > ⁃ A maioria dos frameworks possuem plugins para facilitar a minificação das páginas web. Você pode usar uma porção de módulos do NPM que farão o trabalho pra você automaticamente..

  - 🛠 [Minifcador HTML | Minify Code](http://minifycode.com/html-minifier/)
  - 📖 [Experiências com com Minficador HTML — Perfection Kills](http://perfectionkills.com/experimenting-with-html-minifier/#use_short_doctype) - _(título original:'Experimenting with HTML minifier', em inglês)_

- [ ] **Remover comentários desnecessários:** ![low] Garanta que os comentários serão removidos de suas páginas.

  _Por que:_

  > Comentários não são úteis para o usuário e portanto devem ser removidos dos arquivos de produção. Um caso em que você manteria comentários poderia ser quando precisa manter a origem para uma biblioteca.

  _Como:_

  > ⁃ Na maior parte do tempo, comentários podem ser removidos com um plugin de minificação HTML.

* 🛠 [remove-html-comments - npm](https://www.npmjs.com/package/remove-html-comments)

- [ ] **Remover atributos desnecessários:** ![low] Atributos Type como `type="text/javascript"` ou `type="text/css"` não são mais necessários e devem ser removidos.

  ```html
  <!-- antes do HTML5 -->
  <script type="text/javascript">
      // código Javascript
  </script>

  <!-- Hoje -->
  <script>
      // código Javascript
  </script>
  ```

  _Por que:_

  > Atributos Type não são necessários já que o HTML5 supõe text/css e text/javascript por padrão. Código inutilizado deve ser removido quando não forem usados no seu website ou aplicação por deixarem as páginas mais pesadas.

  _Como:_

  > ⁃ Certifique-se de que todas as _tags_ `<link>` e `<script>` não têm nenhum atributo type.

  - 📖 [A Tag de Script | CSS-Tricks](https://css-tricks.com/the-script-tag/) - _(título original: 'The Script Tag', em inglês)_

- [ ] **Sempre coloque as _tags_ de css antes das de JavaScript:** ![high] Certifique-se de que o seu CSS sempre é carregado antes de ter código JavaScript.

  ```html
  <!-- Não recomendado -->
  <script src="jquery.js"></script>
  <script src="foo.js"></script>
  <link rel="stylesheet" href="foo.css"/>

  <!-- Recomendado -->
  <link rel="stylesheet" href="foo.css"/>
  <script src="jquery.js"></script>
  <script src="foo.js"></script>
  ```

  _Por que:_

  > Ter o CSS antes do Javascript posibilita um melhor download paralelo que torna o tempo de renderização do navegador mais rápido.

  _Como:_

  > ⁃ Certifique-se que as tags `<link>` e `<style>` no `<head>` sempre vêm antes de qualquer `<script>`.

  - 📖 [Ordenando seus estilos e scripts para o carregamento da página](https://varvy.com/pagespeed/style-script-order.html) - _(título original: 'Ordering your styles and scripts for pagespeed', em inglês)_

- [ ] **Reduza a quantidade de iframes:** ![high] Somente use iframes se não há nenhuma outra possibilidade técnica. Evite tanto quanto o possível utilizar iframes.

**[⬆ Topo](#table-of-contents)**

## CSS

![css]

- [ ] **Minificação:** ![high] Todos os arquivos CSS está minificado, comentários, _white spaces_ e novas linhas são removidas dos arquivos de produção.

  _Por que:_

  > Quando os arquivos CSS são minificados, o conteúdo é carregado mais rapidamente e menos dados são enviados ao cliente. É importante sempre minificar os arquivos CSS em produção.Isso é benéfico para o usuário e também para negócios que desejam dimminuir o custo de banda e reduzir o uso de recursos.

  _Como:_

  > ⁃ Use ferramentas para minificar seus arquivos automaticamente antes ou durante o _build_ ou _deploy_.

  - 🛠 [cssnano: Um minificador modular baseado no ecossistema PostCSS](https://cssnano.co/) - _(título original: 'cssnano: A modular minifier based on the PostCSS ecosystem.', em inglês)_
  - 🛠 [@neutrinojs/style-minify - npm](https://www.npmjs.com/package/@neutrinojs/style-minify)

- [ ] **Concatenação:** ![medium] Arquivos CSS são concatenados em um único arquivo _(Nem sempre é válido para HTTP/2)_.

  ```html
  <!-- Não recomendado -->
  <script src="foo.js"></script>
  <script src="ajax.js"></script>

  <!-- Recomendado -->
  <script src="combined.js"></script>
  ```

  _Por que:_

  > Se ainda estiver usando HTTP/1, você talvez precise concatenar seus arquivos, é menos indicado se o seu servidor usa HTTP/2 (é necessário testar).

  _Como:_

  > ⁃ Use uma ferramenta online ou algum plugin antes ou durante o _build_ ou _deploy_ do seu projeto para concatenar arquivos.
  > ⁃ Certifique-se, claro, que a concatenação não quebre o seu projeto.

  - 📖 [HTTP: Otimizando a Entrega de Aplicações - Alta performance em Conexão do Navegador(O'Reilly)](https://hpbn.co/optimizing-application-delivery/#optimizing-for-http2) - _(título original: "HTTP: Optimizing Application Delivery - High Performance Browser Networking (O'Reilly)', em inglês)_
  - 📖 [Melhores Práticas de Performance na Era do HTTP/2](https://deliciousbrains.com/performance-best-practices-http2/) _(título original: 'Performance Best Practices in the HTTP/2 Era', em inglês)_

- [ ] **Não-obstrusivo:** ![high] Arquivos CSS precisam ser não-obstrusivos para prevenir que o DOM demore de carregar .

  ```html
  <link rel="preload" href="global.min.css" as="style" onload="this.rel='stylesheet'">
  <noscript><link rel="stylesheet" href="global.min.css"></noscript>
  ```

  _Por que:_

  > Arquivos CSS podem bloquear o carregamento da página e atrasar a renderização da sua página. Usar `preload` pode carregar os arquivos CSS antes que o navegador comece a mostrar o conteúdo da página.

  _Como:_

  > ⁃ Você precisa adicionar o atributo `rel` com o valor `preload` e incluir `as="style"` no elemento `<link>`.

  - 📖 [loadCSS por filament group](https://github.com/filamentgroup/loadCSS)
  - 📖 [Exemplo de pré-carregamento de CSS usando loadCSS](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf) - _(título original:'loadCSS by filament group', em inglês)_
  - 📖 [Pré-carregamento de conteúdo com rel="preload"](https://developer.mozilla.org/en-US/docs/Web/HTML/Preloading_content) - _(título original:'loadCSS by filament group', em inglês)_
  - 📖 [Pré-carregamento: Pra que serve? — Smashing Magazine](https://www.smashingmagazine.com/2016/02/preload-what-is-it-good-for/) - _(título original:'loadCSS by filament group', em inglês)_

- [ ] **Tamanho das classes CSS:** ![low] O tamanho das suas classes pode causar (baixo) impacto nos seus arquivos HTML e CSS (eventualmente).

  _Por que:_

  > Até mesmo os impactos de performance podem ser contestados, tomar uma decisão sobre a estratégia de nomenclatura do seu projeto pode ter um impacto não trivial na manutenção das suas folhas de estilo. Se estiver usando BEM, em alguns casos, você pode acabar com classes que possuem mais caracteres do que precisam. É sempre importante escolher com sabedoria os nomes e _namespaces_.

  _Como:_

  > ⁃ Definir um limite em termos de número de caracteres pode ser interressante para algumas pessoas, mas garantir que você desmembrou o seu website em componentes pode ajudar a reduzir a quantidade de classes (e declarações) e o tamanho das suas classes.

  - 🛠 [classe longa vs curta · jsPerf](https://jsperf.com/long-vs-short-class) - _(título original:'long vs short class', em inglês)_

- [ ] **CSS inutilizado:** ![medium] Remova seletores CSS inutlizados.

  _Por que:_

  > Remover seletores CSS inutilizados pode reduzir o peso dos seus arquivos e acelerar o carregamento dos seus _assets_.

  _Como:_

  > ⁃ ⚠️ Sempre verifique se o framework de CSS que você quer usar já não possui código de _reset/normalize_. Às vezes você pode não precisar de tudo que está incluído no arquivo de _reset/normalize_.

  - 🛠 [UnCSS Online](https://uncss-online.com/)
  - 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
  - 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
  - 🛠 [Cobertura das Ferrramentas de Desenvolvedor do Chrome](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage) - _(título original: 'Chrome DevTools Coverage', em inglês)_

* [ ] **CSS Crítico:** ![high] O CSS crítico (ou "sobre a dobra") contém todo o CSS usado para renderizar a parte visível da página. ele é incorporado antes da chamada principal do seu CSS e entre `<style></style>` numa única linha (minificado se possível).

  _Por que:_

  > Deixar o CSS crítico _inline_ ajuda a acelerar a renderização de páginas web reduzindo o número de requisições ao servidor.

  _Como:_

  > ⁃ Gere o CSS crítico com ferramentas online ou usando um plugin como o que Addy Osmani desenvolveu.

  - 📖 [Entendendo o CSS Crítico](https://www.smashingmagazine.com/2015/08/understanding-critical-css/) - _(título original: 'Understanding Critical CSS', em inglês)_
  - 🛠 [Critical por Addy Osmani no GitHub](https://github.com/addyosmani/critical) automatiza isso.
  - 📖 [Deixando o CSS crítico _inline_ para ter melhor performance na web | Go Make Things](https://gomakethings.com/inlining-critical-css-for-better-web-performance/) - _(título original: 'Inlining critical CSS for better web performance', em inglês)_
  - 📖 [Gerador de CSS de Caminho Crítico Critical - Priorize contéudo acima da dobra :: SiteLocity](https://www.sitelocity.com/critical-path-css-generator) - _(título original: ' Path CSS Generator - Prioritize above the fold content', em inglês)_

- [ ] **CSS incorporado ou _inline_:** ![high] Evite usar CSS incorporado ou _inline_ dentro do seu `<body>` _(não válido para HTTP/2)_

  _Por que:_

  > Uma das principais razões é que é boa prática **separar conteúdo de design**. Também te ajuda a ter um código mais sustentável e mantém o seu site aceesível. Mas com relação a performance, é simplesmente por diminuir o peso do arquivo das suas páginas HTML e tempo de carregamento.

  _Como:_

  > ⁃ Sempre use folhas de estilo externas ou incorpore o CSS no seu `<head>` (e siga as outras regras de performance).

  - 📖 [Observe as Melhores Práticas de CSS: Evite Usar Estilos CSS _Inline_](https://www.lifewire.com/avoid-inline-styles-for-css-3466846) - _(título original: 'Observe CSS Best Practices: Avoid CSS Inline Styles', em inglês)_

- [ ] **Analyse stylesheets complexity:** ![high] Analyzing your stylesheets can help you to flag issues, redundancies and duplicate CSS selectors.

  _Why:_

  > Sometimes you may have redundancies or validation errors in your CSS, analysing your CSS files and removed these complexities can help you to speed up your CSS files (because your browser will read them faster)

  _How:_

  > ⁃ Your CSS should be organized, using a CSS preprocessor can help you with that. Some online tools listed above can also help you analysing and correct your code.

  - 🛠 [TestMyCSS | Optimize and Check CSS Performance](http://www.testmycss.com/)
  - 📖 [CSS Stats](https://cssstats.com/)
  - 🛠 [macbre/analyze-css: CSS selectors complexity and performance analyzer](https://github.com/macbre/analyze-css)

**[⬆ back to top](#table-of-contents)**

## Fontes

![fonts]

- 📖 [A Book Apart, Webfont Handbook](https://abookapart.com/products/webfont-handbook)

* [ ] **Webfont formats:** ![medium] You are using WOFF2 on your web project or application.

  _Why:_

  > According to Google, the WOFF 2.0 Web Font compression format offers 30% average gain over WOFF 1.0. It's then good to use WOFF 2.0, WOFF 1.0 as a fallback and TTF.

  _How:_

  > ⁃ Check before buying your new font that the provider gives you the WOFF2 format. If you are using a free font, you can always use Font Squirrel to generate all the formats you need.

  - 📖 [WOFF 2.0 – Learn more about the next generation Web Font Format and convert TTF to WOFF2](https://gist.github.com/sergejmueller/cf6b4f2133bcb3e2f64a)
  - 🛠 [Create Your Own @font-face Kits » Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)
  - 📖 [Using @font-face | CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/?ref=frontendchecklist)
  - 📖 [Can I use... WOFF2](https://caniuse.com/#feat=woff2)

* [ ] **Use `preconnect` to load your fonts faster:** ![medium]

  ```html
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  ```

  _Why:_

  > When you arrived on a website, your device needs to find out where you site live and which server it needs to connect with. Your browser had to contact a DNS server and wait for the lookup complete before fetching the ressource (fonts, CSS files...). Prefetches and preconnects allow the browser

  _How:_

  > ⁃ Before prefetching your webfonts, use webpagetest to evaluate your website.
  > ⁃ Look for teal colored DNS lookups and note the host that are being requested.
  > ⁃ Prefetch your webfonts in your `<head>` and add eventually these hostnames that you should prefetch too.

  - 📖 [Faster Google Fonts with Preconnect - CDN Planet](https://www.cdnplanet.com/blog/faster-google-webfonts-preconnect/)
  - 📖 [Make Your Site Faster with Preconnect Hints | Viget](https://www.viget.com/articles/make-your-site-faster-with-preconnect-hints/)
  - 📖 [Ultimate Guide to Browser Hints: Preload, Prefetch, and Preconnect - MachMetrics Speed Blog](https://www.machmetrics.com/speed-blog/guide-to-browser-hints-preload-preconnect-prefetch/)
  - 📖 [A Comprehensive Guide to Font Loading Strategies—zachleat.com](https://www.zachleat.com/web/comprehensive-webfonts/#font-face)

* [ ] **Webfont size:** ![medium] Webfont sizes don't exceed 300kb (all variants included)

- 📖 [Font Bytes - Page Weight](https://httparchive.org/reports/page-weight#bytesFont)

**[⬆ back to top](#table-of-contents)**

## Imagens

![images]

- 📖 [Image Bytes in 2018](https://httparchive.org/reports/page-weight#bytesImg)

- [ ] **Images optimization:** ![high] Your images are optimized, compressed without direct impact to the end user.

  _Why:_

  > Optimized images load faster in your browser and consume less data.

  _How:_

  > ⁃ Try using CSS3 effects when it's possible (instead of a small image)
  > ⁃ When it's possible, use fonts instead of text encoded in your images
  > ⁃ Use SVG
  > ⁃ Use a tool and specify a level compression under 85.

  - 📖 [Image Optimization | Web Fundamentals | Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization)
  - 🛠 [TinyJPG – Compress JPEG images intelligently](https://tinyjpg.com/)

* [ ] **Images format:** ![high] Choose your image format appropriately.

  _Why:_

  > To ensure that your images don't slow your website, choose the format that will

  _How:_

  > ⁃ Use [Lighthouse](https://developers.google.com/web/tools/lighthouse/) to identify which images can eventually use **next-gen formats** (like JPEG 2000m JPEG XR or WebP)
  > ⁃ Compare different formats, sometimes using PNG8 is better than PNG16, sometimes it's not.

  - 📖 [Serve Images in Next-Gen Formats  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/lighthouse/audits/webp)
  - 📖 [What Is the Right Image Format for Your Website? — SitePoint](https://www.sitepoint.com/what-is-the-right-image-format-for-your-website/)
  - 📖 [PNG8 - The Clear Winner — SitePoint](https://www.sitepoint.com/png8-the-clear-winner/)
  - 📖 [8-bit vs 16-bit - What Color Depth You Should Use And Why It Matters - DIY Photography](https://www.diyphotography.net/8-bit-vs-16-bit-color-depth-use-matters/)

- [ ] **Use vector image vs raster/bitmap:** ![medium] Prefer using vector image rather than bitmap images (when possible).

  _Why:_

  > Vector images (SVG) tend to be smaller than images and SVG's are responsive and scale perfectly. These images can be animated and modified by CSS.

* [ ] **Images dimensions:** ![medium] Set `width` and `height` attributes on `<img>` if the final rendered image size is known.

  _Why:_

  > If height and width are set, the space required for the image is reserved when the page is loaded. However, without these attributes, the browser does not know the size of the image, and cannot reserve the appropriate space to it. The effect will be that the page layout will change during loading (while the images load).

* [ ] **Avoid using Base64 images:** ![medium] You could eventually convert tiny images to base64 but it's actually not the best practice.

  - 📖 [Base64 Encoding & Performance, Part 1 and 2 by Harry Roberts](https://csswizardry.com/2017/02/base64-encoding-and-performance/)
  - 📖 [A closer look at Base64 image performance – The Page Not Found Blog](http://www.andygup.net/a-closer-look-at-base64-image-performance/)
  - 📖 [When to base64 encode images (and when not to) | David Calhoun](https://www.davidbcalhoun.com/2011/when-to-base64-encode-images-and-when-not-to/)
  - 📖 [Base64 encoding images for faster pages | Performance and seo factors](https://varvy.com/pagespeed/base64-images.html)

* [ ] **Lazy loading:** ![medium] Images are lazyloaded (A noscript fallback is always provided).

  _Why:_

  > It will improve the response time of the current page and then avoid loading unnecessary images that the user may not need.

  _How:_

  > ⁃ Use [Lighthouse](https://developers.google.com/web/tools/lighthouse/) to identify how many **images are offscreen**.
  > ⁃ Use a JavaScript plugin like to lazyload your images.

  - 🛠 [verlok/lazyload: Github](https://github.com/verlok/lazyload)
  - 📖 [Lazy Loading Images and Video  |  Web Fundamentals  |  Google Developers](https://developers.google.com/web/fundamentals/performance/lazy-loading-guidance/images-and-video/)
  - 📖 [5 Brilliant Ways to Lazy Load Images For Faster Page Loads - Dynamic Drive Blog](http://blog.dynamicdrive.com/5-brilliant-ways-to-lazy-load-images-for-faster-page-loads/)

* [ ] **Responsive images:** ![medium] Ensure to serve images that are close to your display size.

  _Why:_

  > Small devices don't need images bigger than their viewport. It's recommended to have multiple versions of one image on different sizes.

  _How:_

  > ⁃ Create different image sizes for the devices you want to target.
  > ⁃ Use `srcset` and `picture` to deliver multiple variants of each image.

  - 📖 [Responsive images - Learn web development | MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

**[⬆ back to top](#table-of-contents)**

## JavaScript

![javascript]

- [ ] **JS Minification:** ![high] All JavaScript files are minified, comments, white spaces and new lines are removed from production files _(still valid if using HTTP/2)_.

  _Why:_

  > Removing all unnecessary spaces, comments and break will reduce the size of your JavaScript files and speed up your site's page load times and obviously lighten the download for your user.

  _How:_

  > ⁃ Use the tools suggested below to minify your files automatically before or during your build or your deployment.

  - 📖 [uglify-js - npm](https://www.npmjs.com/package/uglify-js)
  - 📖 [Short read: How is HTTP/2 different? Should we still minify and concatenate?](https://scaleyourcode.com/blog/article/28)

* [ ] **No JavaScript inside:** ![medium] _(Only valid for website)_ Avoid having multiple JavaScript codes embed in the middle of your body. Regroupe your JavaScript code inside external files or eventually in the `<head>` or at the end of your page (before `</body>`).

  _Why:_

  > Placing JavaScript embedded code directly in your `<body>` can slow down your page because it loads while the DOM is being built. The best option is to use external files with `async` or `defer` to avoid blocking the DOM. Another option is to place some scripts inside your `<head>`. Most of the time analytics code or small script that need to load before the DOM gets to main processing.

  _How:_

  > ⁃ Ensure that all your files are loaded using `async` or `defer` and decide wisely the code that you will need to inject in your `<head>`.

  - 📖 [11 Tips to Optimize JavaScript and Improve Website Loading Speeds](https://www.upwork.com/hiring/development/11-tips-to-optimize-javascript-and-improve-website-loading-speeds/)

* [ ] **Non-blocking JavaScript:** ![high] JavaScript files are loaded asynchronously using `async` or deferred using `defer` attribute.

  ```html
  <!-- Defer Attribute -->
  <script defer src="foo.js">

  <!-- Async Attribute -->
  <script async src="foo.js">
  ```

  _Why:_

  > JavaScript blocks the normal parsing of the HTML document, so when the parser reaches a `<script>` tag (particularly is inside the `<head>`), it stops to fech and run it. Adding `async` or `defer` are highly recommended if your scripts are placed in the top of your page but less valuable if just before your `</body>` tag. But it's a good practice to always use these attributes to avoid any performance issue.

  _How:_

  > ⁃ Add `async` (if the script don't rely on other scripts) or `defer` (if the script relies upon or relied upon by an async script) as an attribute to your script tag.
  > ⁃ If your have small scripts, maybe use inline script place above async scripts.

  - 📖 [Remove Render-Blocking JavaScript](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Optimized and updated JS libraries:** ![medium] All JavaScript libraries used in your project are necessary (prefer Vanilla Javascript for simple functionalities), updated to their latest version and don't overwhelm your JavaScript with unnecessary methods.

  _Why:_

  > Most of the time, new versions come with optimization and security fix. You should use the most optimized code to speed up your project and ensure that you'll not slow down your website or app without outdated plugin.

  _How:_

  > ⁃ If your project use NPM packages, [npm-check](https://www.npmjs.com/package/npm-check) is a pretty interesting library to upgrade / update your librairies.

  - 📖 [You may not need jQuery](http://youmightnotneedjquery.com/)
  - 📖 [Vanilla JavaScript for building powerful web applications](https://plainjs.com/)

- [ ] **Check dependencies size limit:** ![low] Ensure to use wisely external librairies, most of the time, you can use a lighter library for a same functionnality.

  _Why:_

  > You may be tempted to use one of the 745 000 packages you can find on [npm](https://www.npmjs.com/), but you need to choose the best package for your needs. For example, MomentJS is an awesome library but with a lot of methods you may never use, that's why Day.js was created. It's just 2kB vs 16.4kB gz for Moment.

  _How:_

  > ⁃ Always compare and choose the best and lighter library for your needs. You can also use tools like [npm trends](http://www.npmtrends.com/) to compare NPM package downloads counts or [Bundlephobia](https://bundlephobia.com/) to know the size of your dependencies.

  - 🛠 [ai/size-limit: Prevent JS libraries bloat. If you accidentally add a massive dependency, Size Limit will throw an error.](https://github.com/ai/size-limit)
  - 📖 [webpack-bundle-analyzer - npm](https://www.npmjs.com/package/webpack-bundle-analyzer)
  - 📖 [Size Limit: Make the Web lighter — Martian Chronicles, Evil Martians’ team blog](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **JavaScript Profiling:** ![medium] Check for performance problems in your JavaScript files (and CSS too).

  _Why:_

  > JavaScript complexity can slow down runtime performance. Identifing these possible issues are essential to offer the smoothest user experience.

  _How:_

  > ⁃ Use the Timeline tool in the Chrome Developer Tool to evaluate scripts events and found the one that may take too much time.

  - 📖 [Speed Up JavaScript Execution  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution)
  - 📖 [JavaScript Profiling With The Chrome Developer Tools — Smashing Magazine](https://www.smashingmagazine.com/2012/06/javascript-profiling-chrome-developer-tools/)
  - 📖 [How to Record Heap Snapshots  |  Tools for Web Developers  |  Google Developers](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots)
  - 📖 [Chapter 22 - Profiling the Frontend - Blackfire](https://blackfire.io/docs/book/22-frontend-profiling)

**[⬆ back to top](#table-of-contents)**

## Servidor

![server-side]

- [ ] **Webpage size < 1500 KB:** ![high] (but ideally < 500 KB) Reduce the size of your page + resources as much as you can.

  _Why:_

  > Ideally you should try to target < 500 KB but the state of web shows that the median of Kilobytes is around 1500 KB (even on mobile). Depending your target users, connexion, devices, it's important to reduce as much as possible your total Kilobytes to have the best user experience possible.

  _How:_

  > ⁃ All the rules inside the Front-End Performance Checklist will help you to reduce as much as possible your resources and your code.

  - 📖 [Page Weight](https://httparchive.org/reports/page-weight#bytesTotal)
  - 🛠 [What Does My Site Cost?](https://whatdoesmysitecost.com/)

- [ ] **Page load times < 3 seconds:** ![high] Reduce as much as possible your page load times to quickly deliver your content to your users.

  _Why:_

  > Faster your website or app is, less you have probability of bounce increases, in other terms you have less chances to lose your user or future client. Enough researches on the subject prove that point.

  _How:_

  > ⁃ Use online tools like [Page Speed Insight](https://developers.google.com/speed/pagespeed/insights/) or [WebPageTest](https://www.webpagetest.org/) to analyze what could be slowing you down and use the Front-End Performance Checklist to improve your load times.

  - 🛠 [Compare your mobile site speed](https://www.thinkwithgoogle.com/feature/mobile/)
  - 🛠 [Test Your Mobile Website Speed and Performance - Think With Google](https://testmysite.thinkwithgoogle.com/?_ga=1.155316027.1489996091.1482187369)
  - 📖 [Average Page Load Times for 2018 - How does yours compare? - MachMetrics Speed Blog](https://www.machmetrics.com/speed-blog/average-page-load-times-websites-2018/)

- [ ] **Time To First Byte < 1.3 seconds:** ![high] Reduce as much as you can the time your browser waits before receiving data.

  - 📖 [What is Waiting (TTFB) in DevTools, and what to do about it](https://scaleyourcode.com/blog/article/27)
  - 📖 [Monitoring your servers with free tools is easy](https://scaleyourcode.com/blog/article/7)

* [ ] **Cookie size:** ![medium] If you are using cookies be sure each cookie doesn't exceed 4096 bytes and your domain name doesn't have more than 20 cookies.

  _Why:_

  > cookies is exchanged in the HTTP headers between web servers and browsers. It's important to keep the size of cookies as low as possible to minimize the impact on the user's response time.

  _How:_

  > ⁃ Eliminate unnecessary cookies

  - 📖 [Cookie specification: RFC 6265](https://tools.ietf.org/html/rfc6265)
  - 📖 [Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
  - 🛠 [Browser Cookie Limits](http://browsercookielimits.squawky.net/)
  - 📖 [Website Performance: Cookies Don't Taste So Good - Monitis Blog](http://www.monitis.com/blog/website-performance-cookies-dont-taste-so-good/)
  - 📖 [Google's Web Performance Best Practices #3: Minimize Request Overhead - GlobalDots Blog](https://www.globaldots.com/googles-web-performance-best-practices-3-minimize-request-overhead/)

- [ ] **Minimizing HTTP requests:** ![high] Always ensure that every file requested are essential for you website or application.

- [ ] **Use a CDN to deliver your assets:** ![medium] Use a CDN to deliver faster your content over the world.

* 📖 [10 Tips to Optimize CDN Performance - CDN Planet](https://www.cdnplanet.com/blog/10-tips-optimize-cdn-performance/)
* 📖 [HTTP Caching  |  Web Fundamentals  |  Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching)

- [ ] **Serve files from the same protocol:** ![high] Avoid having your website using HTTPS and serve files coming from source using HTTP.

- [ ] **Serve reachable files:** ![high] Avoid requesting unreachable files (404).

- [ ] **Set HTTP cache headers properly:** ![high] Set HTTP headers to avoid expensive number of roundtrips between your browser and the server.

- [ ] **GZIP compression is enable:** ![high]

* 📖 [Check GZIP compression](https://checkgzipcompression.com/)

**[⬆ back to top](#table-of-contents)**

---

## Frameworks JS e Performance

### Vue

### React

- 📖 [Optimizing Performance - React](https://reactjs.org/docs/optimizing-performance.html)
- 📖 [React image manipulation | Cloudinary](https://cloudinary.com/documentation/react_image_manipulation)
- 📖 [Debugging React performance with React 16 and Chrome Devtools.](https://building.calibreapp.com/debugging-react-performance-with-react-16-and-chrome-devtools-c90698a522ad)

---

## Traduções

The Front-End Performance Checklist wants to also be available in other languages! Don't hesitate to submit your contribution!

## Contribuir

**Open an issue or a pull request to suggest changes or additions.**

## Suporte

If you have any question or suggestion, don't hesitate to use Gitter or Twitter:

- [Chat on Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
- [Facebook](https://www.facebook.com/frontendchecklist/)
- [Twitter](https://twitter.com/thedaviddias)

## Author

**Criado com ❤️ por [David Dias](https://github.com/thedaviddias) em [@influitive](https://influitive.com/) 🇨🇦**

**Traduzido para português (brasil) por [Fernando Malaman](https://github.com/fernandofawkes)**

## Contribuintes

This project exists thanks to all the people who contribute. [[Contribute]](.github/CONTRIBUTING.md).

## Licensa de Uso

[MIT](LICENCE.md)

All icons are provided by [Icons8](https://icons8.com/)

**[⬆ back to top](#table-of-contents)**

[logo]: images/logo-front-end-performance-checklist.jpg
[html]: images/html.png
[css]: images/css.png
[fonts]: images/fonts.png
[images]: images/images.png
[javascript]: images/javascript.png
[server-side]: images/server-side.png
[low]: https://front-end-checklist.now.sh/low.svg
[medium]: https://front-end-checklist.now.sh/medium.svg
[high]: https://front-end-checklist.now.sh/high.svg
