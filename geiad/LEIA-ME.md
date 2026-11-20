# GEIA-D · publicação provisória no Vercel

Esta pasta contém a página do autodiagnóstico GEIA-D pronta para publicar.

| Arquivo | Para que serve |
|---|---|
| `index.html` | A página completa (autodiagnóstico, plano de ação, modelos e framework) |
| `vercel.json` | Configuração: endereços limpos e aviso para buscadores não indexarem |
| `robots.txt` | Pede aos buscadores que não indexem a página (publicação provisória) |

Não há instalação nem etapa de build: é um site estático.

## Opção 1 · Pelo GitHub (recomendada, sem terminal)

1. Crie um repositório no GitHub (pode ser privado), por exemplo `geiad`.
2. Envie os três arquivos desta pasta para o repositório (botão **Add file > Upload files**).
3. Entre em vercel.com, faça login com o GitHub e clique em **Add New > Project**.
4. Escolha o repositório `geiad` e clique em **Import**.
5. Em **Framework Preset**, deixe **Other**. Não preencha comandos de build.
6. Clique em **Deploy**. Em cerca de um minuto, o Vercel mostra o endereço (algo como `geiad.vercel.app`).

Para atualizar depois, basta substituir o `index.html` no GitHub: o Vercel publica a nova versão sozinho.

## Opção 2 · Pelo terminal (Vercel CLI)

Com o Node.js instalado, abra o terminal nesta pasta e rode:

```
npx vercel login
npx vercel --prod
```

Responda às perguntas aceitando os padrões. No fim, o terminal mostra o endereço publicado.

## Depois de publicar

- Abra o endereço em uma janela anônima para conferir que a página abre sem login.
- Teste em um celular.
- Coloque o endereço no e-mail de convite aos especialistas, no lugar de `[link da página]`.

## O que funciona fora do Claude

- **Imprimir**: o botão aparece na seção do plano de ação e imprime só o resultado e o checklist. Para salvar em PDF, escolha "Salvar como PDF" na janela de impressão.
- **Baixar Word**: cada modelo pode ser baixado como arquivo `.doc`, que abre no Word e no Google Docs.
- As respostas do autodiagnóstico ficam guardadas apenas no navegador de quem responde. Nada é enviado a um servidor.

## Cuidados durante a coleta

- Não altere a página enquanto os especialistas estiverem avaliando. A banca precisa saber exatamente qual versão foi avaliada.
- Guarde uma cópia do `index.html` publicado (por exemplo, `index_versao_avaliada.html`) para o material suplementar.
- Por ser provisória, a página pede aos buscadores que não a indexem. Quando quiser torná-la pública, apague o `robots.txt`, retire o bloco `headers` do `vercel.json` e a linha `<meta name="robots" ...>` do `index.html`.
