# Google-News-Scraper-via-RSS-HTML-JavaScript-


Google News Scraper via RSS (HTML + JavaScript)
Este projeto é uma aplicação web simples que permite buscar notícias diretamente do Google News com base em um tema digitado pelo usuário. Utiliza RSS feeds, JavaScript puro e um proxy gratuito para contornar restrições de CORS, funcionando 100% no navegador — sem backend ou dependências externas.

🚀 Funcionalidades
Campo de busca para qualquer tema (ex: política, tecnologia, economia)

Requisição ao feed RSS do Google News

Conversão do RSS para JSON via proxy (rss2json.com)

Exibição das notícias com título, link e data

Interface leve e responsiva

🧱 Tecnologias usadas
HTML5: estrutura da página

CSS3: estilo visual simples e limpo

JavaScript (Vanilla): lógica de busca e renderização

RSS2JSON API: proxy para contornar CORS e transformar RSS em JSON

📦 Como usar
Clone ou baixe este repositório

Abra o arquivo index.html no navegador

Digite um tema no campo de busca

Clique em “Buscar” e veja os resultados aparecerem

📄 Código principal (resumo)
javascript
const tema = document.getElementById('tema').value.trim();
const rssUrl = `https://news.google.com/rss/search?q=${encodeURIComponent(tema)}`;
const proxyUrl = `https://api.rss2json.com/v1/api.json?rss_url=${encodeURIComponent(rssUrl)}`;

const res = await fetch(proxyUrl);
const data = await res.json();
const items = data.items;
🧪 Exemplo de uso
Buscar por inteligência artificial retorna as últimas notícias sobre IA publicadas em diversos sites.

Cada resultado inclui:

📰 Título da notícia

🔗 Link direto para o artigo

📅 Data de publicação

⚠️ Limitações
O Google News RSS não permite requisições diretas via navegador (CORS), por isso usamos um proxy.

A API rss2json.com tem limite de uso gratuito — para projetos maiores, recomenda-se usar backend próprio.

💡 Próximos passos (ideias de melhoria)
Exportar resultados para PDF ou CSV

Adicionar histórico de buscas

Suporte a múltiplos idiomas

Versão mobile com design responsivo

Integração com APIs de notícias como GNews, NewsAPI, etc.

📜 Licença
Este projeto é livre para uso e modificação. Sinta-se à vontade para contribuir!
