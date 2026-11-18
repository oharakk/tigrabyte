# Tigrabyte 2.0

Site estático completo, criado a partir do backup do Blogger em 18/11/2026.

- **17 artigos originais importados**, com texto completo e links preservados.
- **1 artigo novo** sobre Duolingo, com ilustrações identificadas como imagens geradas por IA.
- Imagens de capa e imagens internas convertidas para WebP, hospedadas localmente.
- Páginas individuais em `posts/<slug>/index.html`.
- Busca, filtro de categorias, seção "Mais baixados" editorial e layout responsivo.
- Botão de TikTok em duas etapas, contagem de 30s e link de arquivo original; opcional acesso direto e aviso de afiliação.
- `data/links_originais.csv` para auditoria dos links herdados.

## Visualizar localmente

Abra `index.html` no navegador. Páginas e assets usam caminhos relativos. Para testar comportamento de busca e navegação em servidor, rode `python -m http.server 8000` na pasta raiz e abra `http://localhost:8000`.

## Publicar no GitHub Pages

Crie um repositório, adicione todos os arquivos (incluindo pastas `posts`, `assets`, `data`), ative GitHub Pages em **Settings > Pages > Deploy from a branch > main / (root)**. URLs ficam no formato `https://usuario.github.io/repositorio/`. Observe as regras e limites do GitHub Pages aplicáveis a sites comerciais.

## Publicar no Cloudflare Pages

Conecte o mesmo repositório no Cloudflare Pages. Para site estático puro, configure framework **None**, nenhum comando de build e **Build output directory: `.`** (a pasta raiz do projeto) conforme a interface de configuração. Não coloque um framework/build de Astro: este projeto já está pronto em HTML/CSS/JS.

## Limitações honestas

- O backup não traz estatísticas de downloads. A seção **Mais baixados** mostra seleção editorial **sem número inventado**. Para ordenar por dados reais, adicione analytics/counter autorizado depois do deploy.
- A contagem do TikTok **não confirma participação**. É um timer local. Não prometemos que links originais funcionem ou sejam seguros.
- **3 publicações contêm links encurtados** e **2 dependem apenas deles** para o botão final; todos foram mantidos como estavam no backup.
- O artigo original do Spotify não tinha título no arquivo XML; um título editorial foi reconstruído, mas o corpo é original.
- Textos com alegações sobre APKs, mods e disponibilidade foram preservados do arquivo histórico, **não verificados**. Cuidado com direitos de distribuição e políticas da hospedagem.
- Isto é um site estático, sem painel CMS. Novos posts exigem editar arquivos ou integrar um CMS.
- Os arquivos originais `.apk`, jogos e executáveis não fazem parte deste pacote; apenas links externos foram preservados.

## Para migrar SEO

Identifique a URL definitiva e o endereço antigo de cada artigo antes de gerar `sitemap.xml` e redirecionamentos permanentes. O backup do Blogger não contém métricas de tráfego, URLs canônicas completas ou Analytics. Não altere DNS do blog antigo antes de testar a nova versão.
