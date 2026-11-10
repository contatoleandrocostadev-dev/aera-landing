# Landing page da AERA: pacote para publicar

Conteúdo: `index.html` (página completa), `assets/` (logos, imagem de compartilhamento, ícones), `robots.txt`, `sitemap.xml`.

## 1. Endereço público (faça antes de publicar)
Os arquivos assumem o endereço `https://contatoleandrocostadev-dev.github.io/aera-landing/`.
Se a página for para outro endereço, troque esse texto, em todos os lugares, por um localizador do editor, em:
`index.html` (canonical, og:url, og:image, twitter:image e dados estruturados), `robots.txt` e `sitemap.xml`.

## 2. Publicar no GitHub Pages
Crie um repositório (por exemplo `aera-landing`), envie o conteúdo desta pasta na raiz e ative Settings > Pages > Deploy from a branch > main / root.

## 3. Formulário de contato
O envio usa o serviço FormSubmit, que entrega as mensagens em contato.leandrocosta.dev@gmail.com.
Na primeira vez, envie uma mensagem de teste pela página publicada e clique no link de confirmação que chegará nesse e-mail. Até confirmar, os envios não são entregues e a página mostra o botão "Enviar pelo meu e-mail" como alternativa.
Para usar outro serviço, troque a constante `ENDPOINT` no início do script de `index.html`.

## 4. Logos institucionais
Em `index.html`, procure por "LOGOS" e troque o conteúdo de cada `<div class="slot">` por
`<img src="assets/logo-ufla.png" alt="Universidade Federal de Lavras" height="56">` (e o equivalente do Avança Café).
Use apenas logos que você tenha autorização para exibir.

## 5. Depois de publicar
Teste o cartão de compartilhamento no depurador de links do Facebook/LinkedIn e no validador de cards do X, e envie o sitemap no Google Search Console.

## Publicar no GitHub Pages (vira link)
1. Crie um repositório em github.com/new (ex.: `aera-landing`, público).
2. Na pasta deste pacote (onde está o `index.html`), no terminal:
   ```
   git init
   git add .
   git commit -m "Landing page AERA"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/aera-landing.git
   git push -u origin main
   ```
   (Sem terminal: no repositório, **Add file → Upload files**, arraste todo o conteúdo da pasta e faça o commit.)
3. No repositório: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save**.
4. Em 1 a 2 minutos o site fica em `https://SEU-USUARIO.github.io/aera-landing/`.
5. Se o endereço for diferente de `https://contatoleandrocostadev-dev.github.io/aera-landing/`, troque essa URL no `index.html` (canonical, og:url, og:image, JSON-LD), em `sitemap.xml` e `robots.txt`.

## Formulário para planilha
Veja `apps-script/GUIA.md`.
