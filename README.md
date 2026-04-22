# Programmering för UX-Produktion 2026

## Lektion 5

Under lektion 5 har vi främst jobbat med CSS Grid. Vi började med att kika på Figma's nya Grid-verktyg och pratade om hur man kan tänka när man bygger upp en layout med hjälp av rader och kolumner.

Vi gjorde sedan en övning där vi först återskapade ett bento-grid i Figma och därefter byggde samma layout i kod. Under lektionen testade vi både att använda CSS Grid manuellt med vanlig CSS och att använda grid-klasser med hjälp av Tailwind.

## Vi har under lektionen:

- Kikat på Figma's Grid-verktyg
- Pratat om hur man tänker när man bygger layouter med grid
- Återskapat ett bento-grid i Figma
- Byggt samma bento-grid i kod
- Testat CSS Grid både med vanlig CSS och med Tailwind
- Kikat på en responsiv layout med `grid-template-areas`

## CSS Grid

CSS Grid används för att skapa layouter med hjälp av kolumner och rader. Till skillnad från Flexbox, som oftast är bäst när vi vill placera saker i en riktning åt gången, är Grid väldigt bra när vi vill bygga upp hela ytor och mer avancerade layouter.

Man kan tänka på det lite som att vi delar upp sidan i ett rutnät och sedan placerar innehåll i olika delar av det rutnätet.

```css
display: grid;
```

## Vanliga Grid-properties vi använde

### grid-template-columns

Används för att bestämma hur många kolumner vårt grid ska ha och hur breda de ska vara.

```css
grid-template-columns: 1fr 1fr 1fr 1.3fr;
```

Här skapar vi 4 kolumner där den sista kolumnen är lite bredare än de andra.

Vi nämnde även att man ibland kan skriva samma sak kortare med `repeat()`. detta kräver dock att alla de kolumner man vill repetera har samma storlek

```css
grid-template-columns: repeat(4, 1fr);
```

### grid-template-rows

Används för att bestämma hur många rader vårt grid ska ha och hur höga de ska vara.

```css
grid-template-rows: 1fr 0.8fr 0.2fr 1fr;
```

### gap

`gap` används för att skapa mellanrum mellan rutorna i vårt grid på precis samma sätt som med flexbox eller Auto Layout i Figma.

```css
gap: 24px;
```

### height: 100svh

Vi använde även:

```css
height: 100svh;
```

Detta gör att ytan fyller hela skärmens höjd.

## Bento-grid

Vi byggde ett så kallat bento-grid där vissa rutor tar upp mer plats än andra. För att göra detta kunde vi låta vissa element spänna över flera kolumner eller rader.

I Tailwind gjordes detta bland annat med klasser som:

- `col-span-2`
- `row-span-2`
- `row-span-3`

Det betyder att ett element får ta upp flera kolumner eller flera rader i gridet.

## Exempel på ett grid med vanlig CSS

```css
.my-grid {
  height: 100svh;
  display: grid;
  padding: 48px;
  gap: 24px;
  grid-template-columns: 1fr 1fr 1fr 1.3fr;
  grid-template-rows: 1fr 0.8fr 0.2fr 1fr;
}
```

## Exempel på ett bento-grid med Tailwind-klasser

```html
<div class="my-grid">
  <div></div>
  <div class="col-span-2"></div>
  <div class="row-span-2"></div>

  <div class="row-span-2"></div>
  <div class="row-span-2"></div>
  <div class="row-span-3"></div>

  <div class="row-span-2"></div>
  <div class="col-span-2"></div>
</div>
```

## Grid Areas

Vi kikade också på ett annat sätt att bygga layout med Grid, nämligen `grid-template-areas`.

Detta är väldigt användbart när vi har tydliga delar av en sida, tex:

- header
- sidebar
- content
- footer

Då kan vi först namnge områden i vårt grid och sedan koppla varje HTML-element till rätt område.

### Exempel

```css
body {
  display: grid;
  grid-template-areas:
    "header"
    "content"
    "sidebar"
    "footer";
  grid-template-rows: 48px 1fr 200px 150px;
  grid-template-columns: 1fr;
}
```

Sedan kopplar vi elementen till sina områden:

```css
#header {
  grid-area: header;
}

#sidebar {
  grid-area: sidebar;
}

#content {
  grid-area: content;
}

#footer {
  grid-area: footer;
}
```

## Media Queries

Vi använde även en så kallad "media query" för att ändra layouten på större skärmar.

```css
@media screen and (min-width: 600px) {
  body {
    grid-template-areas:
      "header header"
      "sidebar content"
      "footer footer";
    grid-template-rows: 48px 1fr 150px;
    grid-template-columns: 200px 1fr;
  }
}
```

Detta gör att layouten ändras beroende på skärmens bredd. På mindre skärmar ligger innehållet under varandra, medan det på större skärmar delas upp i flera kolumner.

## Overflow

I content-ytan använde vi även:

```css
overflow: auto;
```

Detta gör att innehållet kan scrolla om det blir större än den yta som finns tillgänglig.
