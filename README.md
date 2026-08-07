# Architek — site institucional

Site estático bilíngue (PT/FR) apresentando os dois serviços da Architek:
1. Arquitetura & Automação de Sistemas (projeto personalizado)
2. Programa "Do Zero ao seu SaaS" (3 meses, €6.000)

## Estrutura

```
index.html      → estrutura da página
styles.css       → todo o visual (paleta, tipografia, layout)
script.js        → toggle de idioma PT/FR
assets/          → imagens (foto do fundador)
vercel.json      → configuração de deploy
```

Site 100% estático — sem build, sem dependências, sem framework.

## Como subir no GitHub

```bash
cd architek-repo
git init
git add .
git commit -m "Site inicial Architek"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/architek-site.git
git push -u origin main
```

## Como conectar no Vercel

1. Entre em [vercel.com/new](https://vercel.com/new)
2. Importe o repositório `architek-site` do GitHub
3. Framework Preset: **Other** (não precisa de build command nem output directory)
4. Clique em **Deploy**

A partir daí, todo `git push` na branch `main` gera um deploy novo automaticamente.

## Editar o conteúdo

- Textos em português e francês: procure o objeto `translations` em `script.js` (chaves `pt` e `fr`)
- Preço, seções e estrutura: `index.html`
- Cores, fontes, espaçamento: `styles.css` (variáveis no topo, em `:root`)
- Foto do fundador: substitua `assets/arthur-ximenes.jpg` mantendo o mesmo nome de arquivo

## Pendências antes de publicar

- [ ] Trocar `mailto:arthur@seudominio.com` pelo e-mail real de contato (em `index.html`, seção `#contact`)
- [ ] Trocar o link vazio de "Agendar chamada" por um link real (Calendly, Cal.com, etc.)
- [ ] Definir condições de pagamento do programa de €6.000 (à vista / parcelado)
