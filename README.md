# Programmering för UX-Produktion 2026

# Dag 2 - Samanfattning

## Nya HTML-element som vi kikade på

- `<header>` - Används för att markera inledande innehåll så som tex en meny
- `<main>` - Används för att markera det huvudsakliga/viktigaste innehåller
- `<nav>` - Används för att

### Nämnde dessa men vi har ännu inte anänt dem i koden

- `<footer>` - Används för att markera avslutande innehåll/sidfot
- `<section>` - Används för att markera en tydlig sektion - tex. en sektion av sidan som handlar om nya produkter eller liknande
- `<article>` - Används för att markera innehåll som kan stå helt för sig själv - tex. en artikel, blogginlägg, produktkort etc.
- `<aside>` - Används för att markera innehåll som är relaterat men inte centralt/huvud-innehåll - Tex. en fakta-ruta i en artikel

## CSS Properties vi använde:

### Display Block

Ett element som har `display: block` börjar alltid på en ny rad och tar sedan upp hela bredden oavsett innehållets storlek. Detta "tvingar" efterföljande innehåll på en ny rad oavsett om det efterföljande elementet har display block eller något annat.

```css
display: block;
```

Default inställningen för de flesta grupperande element tex. div, header, footer, main, nav, ul, etc. men även för paragrafer (p), och alla rubriker (h1-h6)

### Display Inline

Ett element som har `display: inline` tar bara upp så mycket bredd som dess innehåll kräver, tänk tex. en länk (a) som ligger mitt i en paragraf-text. Till skillnad från display block så börjar den inte med en ny rad automatiskt och tar bara upp så mycket utrymme på bredden som dess innehåll kräver.

```css
display: inline;
```

Default inställningen för text-element som ofta används innuti/inline med löpande text tex. länkar (a) men även flera andra element som vi inte hunnit kika på ännu.

### Display Flex

Ett element som har `display: flex` motsvarar att vi slagit på `Auto Layout` i Figma. Med hjälp av flexbox kan vi positionera elementets "children" på precis samma sätt som vi är vana vid i Figma.

```css
display: flex;
```

> OBS! Verktyget heter Flexbox men vi skriver alltid bara "flex"!

#### Exempel på en lista med länkar som vi stylat med Flexbox

```html
<ul>
  <li><a href="/">Länk 1</a></li>
  <li><a href="/">Länk 2</a></li>
  <li><a href="/">Länk 3</a></li>
  <li><a href="/">Länk 4</a></li>
  <li><a href="/">Länk 5</a></li>
</ul>
```

```css
ul {
  display: flex; /* Här väljer vi att använda "flexbox" */
  gap: 16px; /* Här ställer vi in avståndet mellan varje länk (16px) */
  justify-content: start; /* Här säger vi att alla länkar ska positioneras längst till vänster/början av listan */
  align-items: center; /* Här säger vi att alla länkar ska centreras vertikalt */
}
```

### Hover-states

```css
a {
  /* här skriver vi vår default-styling för en länk */
}

/* Genom att lägga till ":hover" så kommer denna styling enbart att appliceras när vi hovrar över elementet */
a:hover {
  color: black;
  text-decoration: underline;
}
```
