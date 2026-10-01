# Missão Doomsday

Guia mobile para chegar a **Avengers: Doomsday** sem ter visto o MCU: 23 projetos para ver, com checklist, e 28 notas com spoilers para os projetos que ficam de fora.

É uma PWA estática (HTML, CSS e JS num só ficheiro), sem build. Instala-se no ecrã principal em Android e iOS e funciona offline depois da primeira visita. O progresso fica guardado no telemóvel de cada pessoa.

## Estrutura

```
index.html              app completa
manifest.webmanifest    nome, cores e ícones da app instalada
sw.js                   service worker (cache offline)
icons/                  192, 512, 512 maskable, apple-touch 180, favicon 32
vercel.json             headers do service worker, do manifest e dos ícones
```

## Publicar

1. Cria um repositório no GitHub e envia estes ficheiros para a raiz.
2. Na Vercel: **Add New > Project**, importa o repositório, Framework Preset **Other**, sem build command nem output directory. Deploy.
3. Cada push para `main` publica uma versão nova.

## Atualizar a app

Sempre que alterares o `index.html`, muda `VERSION` no `sw.js` (por exemplo `md-v2`). Assim os telemóveis com a app instalada recebem a versão nova.

## Instalar

- **Android (Chrome):** aparece o botão Instalar na página, ou menu ⋮ > Instalar app.
- **iPhone (Safari):** Partilhar > Adicionar ao ecrã principal.
