# Programmering för UX-Produktion 2026

## Länkar till alla lektioner

| Lektion                                                                                                       |
| ------------------------------------------------------------------------------------------------------------- |
| [Lektion 1](https://github.com/BiggerPixel/UX25-Programmering/tree/lektion-1)                                 |
| [Lektion 2](https://github.com/BiggerPixel/UX25-Programmering/tree/lektion-2)                                 |
| [Lektion 3](https://github.com/BiggerPixel/UX25-Programmering/tree/lektion-3)                                 |
| [Lektion 4](https://github.com/BiggerPixel/UX25-Programmering/tree/lektion-4)                                 |
| [Lektion 4 - Tailwind Intro](https://github.com/BiggerPixel/UX25-Programmering/tree/lektion-4-tailwind-intro) |

## Såhär kommer du igång:

### 1. Ladda ner projektmappen:

- Ladda ner mappen vi kommer att utgå ifrån [här](https://github.com/BiggerPixel/UX25-Programmering/archive/refs/heads/main.zip).
- När mappen laddats ner kan du behöva "unzippa" den.
- Flytta mappen till ett ställe som du lätt hittar tillbaka till. Vi kommer att använda os av denna mapp under alla lektioner så det underlättar mycket om den är lättilgänglig.

### 2. Installera VS Code

- Under kursen kommer vi att använda oss av programmet VS Code för att skriva all kod.
- Om du inte redan har VS Code sedan tidigare laddar du hem det [här](https://code.visualstudio.com/download). (Inte samma program som Visual Studio om du skulle ha detta sedan tidigare.)
- Installera programmet och öppna det.

### 3. Öppna projektmappen:

- Gå till menyn i VS Code `File > Open Folder...` och välj projektmappen du laddade ner i steg 1.
- I vänsterkanten bör du nu se mappens alla filer och du kan nu klicka på filen `index.html`

# Dag 1 - Samanfattning

---

Vi har under kursens första dag:

- [x] Gått igenom kursens innehåll och planering
- [x] Installerat VS Code och öppnat upp projektmappen
- [x] Skapat vår första HTML-Fil (`index.html`)
- [x] Skapat vår första CSS-Fil (`/assets/styles/main.css`)

## Grund-element

Dessa element kommer vi _alltid_ ha med i alla våra HTML-filer

- html
- head - Vi stoppar metadata och länkar till CSS-filer i head-elementet
  - meta - Metadata om sidan
  - title - Används för att namnge sidan, syns i browser-fliken och i historiken
  - link - Används för att tex. länka till en CSS-fil
- body - I body-elementet stoppar vi sidans innehåll (rubriker, texter, bilder, knappar etc.)

## Grupperande Element

- div - Tänk att detta är lite som en tom "Frame" i Figma, vi kan stoppa innehåll i en `div` och sedan styla den som en enhet/grupp

## Rubriker

- h1 - Vi ska alltid ha med 1st h1-element per HTML-sida, men aldrig fler än 1 (Sidans huvudrubrik)
- h2
- h3
- h4
- h5
- h6

## Länk och vanlig text

- a - Används för länkar, antingen mellan våra egna sidor eller till någon annan hemsida på nätet
- p - Använd för paragrafer med text

## Bilder

- img - Använde för att visa en bild

## Listor

- ol - "Ordered List" dvs. Numrerad lista, toppen för att automatiskt få 1. 2. 3. för listor
- ul - "Unordered List" eller "Punktlista", samma som OL fast ingen "numrering".
- li - "List Item" detta används för att skapa varje rad i en lista
