# pedro-kosa-site

Portfólio de Pedro Kosa. Site estático de um arquivo só (`index.html`), sem build.

## Ver no computador

Abra o terminal nesta pasta e rode:

```
python3 -m http.server 8000
```

Depois abra http://localhost:8000. Abrir o index.html direto com duplo clique também funciona, mas o servidor local é mais fiel ao site publicado.

## Trabalhar com o Claude Code

Abra o terminal nesta pasta e rode `claude`. Ele lê o `CLAUDE.md` automaticamente, com as regras do projeto. Para contexto mais fundo, peça para ele ler a pasta `docs/`.

## Publicar (GitHub Pages + domínio .com.br)

1. Registre o domínio no Registro.br e ative a verificação em duas etapas lá e no GitHub.
2. Crie um repositório público no GitHub (por exemplo, `pedro-kosa-site`) e envie esta pasta para ele. O Claude Code pode fazer isso por você com o `gh` instalado.
3. No repositório, vá em Settings > Pages, escolha "Deploy from a branch", branch `main`, pasta `/ (root)`.
4. Ainda em Pages, em "Custom domain", digite o domínio (ex.: `pedrokosa.com.br`). O GitHub cria o arquivo `CNAME` no repositório.
5. No Registro.br, em DNS do domínio, crie quatro registros A apontando para 185.199.108.153, 185.199.109.153, 185.199.110.153 e 185.199.111.153, e um CNAME `www` apontando para `SEU-USUARIO.github.io`. Confira esses valores na documentação do GitHub Pages antes, porque podem mudar.
6. Espere a propagação (de minutos a algumas horas) e marque "Enforce HTTPS" em Pages.
7. Troque `SEU-DOMINIO` nas meta tags Open Graph do `index.html` e crie `assets/og-image.png`.

A partir daí, cada alteração enviada ao GitHub republica o site sozinha.
