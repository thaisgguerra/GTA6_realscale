# GTA VI em escala real 🌴



https://github.com/user-attachments/assets/21cfa294-a663-4c2b-be8c-5d892240b7ae



Uma página interativa que pega os números do jogo mais esperado da década e coloca ao lado de coisas que existem de verdade.

**Leonida é do tamanho de quê? Quanto custou? Quanto tempo levou? Quanta gente trabalhou nisso?** Em vez de responder com uma lista de números, a página deixa você mexer, comparar e descobrir.

> Projeto de fã, feito apenas para fins de entretenimento e informação, sem nenhum objetivo comercial. Não tem vínculo com a Rockstar Games nem com a Take-Two Interactive.

---

## 🎯 Objetivo

Números muito grandes não querem dizer muita coisa sozinhos. "US$ 2 bilhões" ou "212 GB" são difíceis de imaginar.

O objetivo foi **traduzir a escala do GTA VI para referências do dia a dia**: o mapa ao lado de São Paulo e do Rio, o orçamento ao lado de filmes e da missão Apollo 11, o tempo de produção ao lado do que aconteceu no mundo nesse período.

Tudo com a estética de Vice City: neon, modo escuro e muito rosa, roxo e ciano.

## 🧠 Racional: como o projeto foi pensado

**1. Começou como um roteiro de áudio.**
A base foi um roteiro com curiosidades sobre o jogo. A pergunta foi: como transformar isso em algo que a pessoa explora, em vez de só ouvir ou ler?

**2. Cada número virou uma comparação.**
Cada seção pega um fato e responde "isso é grande comparado a quê?". Quando um número era estimativa, a página diz isso de forma clara.

**3. A página conta uma história em 4 partes.**
As 15 seções seguem uma ordem narrativa:

| Parte | Seções |
|---|---|
| 1. A escala | Mapa, grana, tempo, equipe |
| 2. Os bastidores | Pesquisa, tecnologia |
| 3. O mundo | História, bichos, polícia, carros, marcas |
| 4. O lançamento | Trilha sonora, marketing, segredo, resumo |

**4. Informação com fonte.**
Os dados vêm de reportagens (Bloomberg, Game Informer, Forbes, entre outras) e de anúncios oficiais da Rockstar. Números de vendas e pré-vendas são estimativas de mercado e aparecem com esse aviso. As fontes estão listadas no final da página.

**5. Interação com propósito.**
Cada recurso interativo existe para ajudar a entender um dado:

- arrastar o orçamento e ver o que ele compraria;
- tocar nos pedestres 3D e ver a "ficha" de cada um;
- girar o dial das rádios do jogo;
- montar a garagem com os carros inspirados em modelos reais;
- simular as estrelas de procurado da polícia.

**6. Feito com apoio de IA.**
O projeto foi desenvolvido com o Claude (Anthropic) como parceiro de pesquisa, escrita e código. As decisões de produto, conteúdo e design foram da autora: o que contar, em que ordem, com qual estética e o que cortar.

## ✨ Destaques

- **Bilíngue:** abre em português, com botão para inglês.
- **Responsiva:** funciona do celular ao desktop.
- **Abertura cinematográfica:** zoom lento no fundo, paralaxe com o mouse, letreiros neon que piscam, luzes da cidade e aviões cruzando o céu.
- **Modo anoitecer e amanhecer:** cada modo tem a sua própria foto de fundo.
- **Pedestres em 3D:** hologramas animados com caminhada humana real.
- **Acessível:** respeita a opção de "reduzir movimento", tem textos alternativos nas imagens e navegação por teclado.

## 🛠️ Como foi feito

- **HTML, CSS e JavaScript puros**, sem framework.
- **Canvas e SVG** para gráficos e animações.
- **three.js** só para os pedestres 3D. Ele carrega apenas quando a pessoa chega perto da seção.
- **Imagens em WebP**, carregadas sob demanda, para a página abrir rápido.
- **Fontes:** Anton, Archivo, Mr Dafoe e Sora, via Google Fonts.

### Desempenho

Ao abrir a página, o navegador baixa só o HTML (cerca de 360 KB) e a imagem do topo. O resto (fotos, modelo 3D, imagens das seções) só carrega quando a pessoa rola até lá.

## 🚀 Como rodar

Não precisa instalar nada.

```bash
# opção 1: abrir direto
# dê dois cliques no index.html

# opção 2: servidor local
python3 -m http.server 8000
# e abra http://localhost:8000
```

### Publicar no GitHub Pages

1. Suba o `index.html` e a pasta `assets` para o repositório.
2. Vá em **Settings → Pages**.
3. Em **Source**, escolha a branch `main` e a pasta raiz.
4. Em alguns minutos, o site fica disponível em `https://seu-usuario.github.io/nome-do-repo`.

## 📁 Estrutura

```
├── index.html     # página completa (HTML, CSS e JS)
├── assets/        # imagens e scripts carregados sob demanda
│   ├── *.webp / *.jpg
│   ├── npc3d.js   # motor 3D dos pedestres (three.js)
│   └── man.js     # modelo 3D Cesium Man
└── README.md
```

## 📜 Créditos e licenças

- **Modelo 3D dos pedestres:** Cesium Man, © Cesium, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), sem a textura original.
- **Foto do jacaré:** Djngsf, CC BY-SA 4.0, via Wikimedia Commons.
- **Foto do macaco-rhesus:** Anoldent, CC BY-SA 2.0, via Wikimedia Commons.
- **Foto de Bonnie e Clyde:** cerca de 1933, domínio público.
- **Fotos do diário de pesquisa:** Pexels (licença Pexels).
- **Imagens das armas:** guia da DriveUpdate, usadas como ilustração.
- **Artes, capturas e marcas do jogo:** © Rockstar Games, usadas apenas como referência.

Grand Theft Auto, GTA e Rockstar Games são marcas dos seus respectivos donos.

## 👩‍💻 Autora

Feito por **[Thais Guerra](https://linkedin.com/in/thais-guerra)**, do Brasil 🇧🇷
