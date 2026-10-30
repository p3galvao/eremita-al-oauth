# OAuth Consent Pages — Eremita AL Management

Estas páginas são exigidas pelo **Google Cloud Console** para publicar a app
OAuth 2.0 em modo **Production**.

## O que é esta app?

A **Eremita AL Management** é uma app interna que liga o Google Calendar,
Sheets e Drive ao back-office do Alojamento Local em Peniche.
Essencial para as cron jobs (checkouts, lembretes) do Mr. Eremita.

## O que contém esta pasta

| Ficheiro | Para que serve |
|---|---|
| `index.html` | Página inicial — aparece no ecrã de consentimento OAuth |
| `privacy.html` | Política de Privacidade — obrigatório para publicar em Production |

## Como usar

1. Fazer push deste repositório para o GitHub
2. Ativar **GitHub Pages** em Settings → Pages (branch `main`, `/ (root)`)
3. Pegar no URL (ex: `https://<user>.github.io/eremita-al-oauth/`)
4. Meter no Google Cloud Console → OAuth consent screen:
   - **Home page URL**: `https://<user>.github.io/eremita-al-oauth/`
   - **Privacy Policy URL**: `https://<user>.github.io/eremita-al-oauth/privacy`
5. Clicar **Publish App → In Production**

## Notas

- O GitHub Pages gratuito só funciona em **repositórios públicos**
- Depois de publicado, os refresh tokens OAuth deixam de expirar a cada 7 dias
- Se precisares de atualizar as páginas, edita aqui e faz push — o GitHub Pages
  atualiza automaticamente em 1-2 minutos