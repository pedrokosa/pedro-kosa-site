# Decisões iniciais (resumo da primeira conversa)

Resumo das decisões tomadas antes da construção do site. A transcrição completa está no Project "Site portfolio" no claude.ai.

## Por que site próprio e não Notion
O Notion só aceita domínio próprio em plano pago (cerca de US$ 18 a 20 por mês) e não permite HTML, CSS ou JavaScript customizados. Como o visual faz parte da mensagem, a escolha foi site próprio feito com IA. Custo fixo: só o domínio, perto de R$ 40 por ano.

## Infraestrutura escolhida
Domínio: .com.br no Registro.br (aceita CPF). Registrar também o .com só se fizer sentido atender clientes de fora.
Código: repositório no GitHub.
Hospedagem: GitHub Pages (gratuito, exige repositório público no plano gratuito). Alternativa se quiser repositório privado: Cloudflare Pages.
Segurança: site estático não tem servidor nem banco para invadir. O risco está nas contas, então ativar verificação em duas etapas no GitHub e no Registro.br.

## Contato
WhatsApp como canal principal (link wa.me com mensagem pré-preenchida), e-mail como secundário. Ideal usar WhatsApp Business ou número separado. Sem formulário por enquanto.

## Analytics
Google Analytics (GA4) é gratuito: criar conta, pegar o ID G-XXXXXXX e colar o trecho no HTML. Usa cookies, então pede um aviso simples de privacidade por causa da LGPD. Alternativa sem cookies e gratuita: Cloudflare Web Analytics.

## Ainda faltava (segundo a conversa)
SEO básico (título, descrição, Open Graph, favicon, sitemap), imagens otimizadas em WebP, e-mail com o domínio (opcional) e o passo a passo de deploy.
