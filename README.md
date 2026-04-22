# Programmering för UX-Produktion 2026

## Tailwind Intro

Under denna lektion introducerar vi Tailwind för första gången och får tillgång till deras så kallade "utillity-klasser" genom att länka till deras styling.

I vår [index.html](/index.html) fil hittar vi grunden för att kunna börja använda Tailwind, det gör vi genom att länka till deras styling på ett liknande sätt som vi tidigare har länkat till vår egen CSS-fil

> Notera här att det görs på ett lite annorlunda sätt med en `<script>` tag istället för `<link>` som vi tidigare använt.

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <!-- Här länkar vi till Tailwind-stylingen -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  </head>
  <body>
    <!-- Här placerar vi vårt innehåll -->
  </body>
</html>
```

## Tailwind-klasser

### Text-storlekar

För att justera storleken på texter testade vi att använda Tailwinds `text-*` klasser för storlekar

| class       | font-size | line-height |
| ----------- | --------: | ----------: |
| `text-4xl`  |      36px |        40px |
| `text-3xl`  |      30px |        36px |
| `text-lg`   |      18px |        28px |
| `text-base` |      16px |        24px |

[Läs mer om klasser för textstorlekar](https://tailwindcss.com/docs/font-size)

### Tecken-vikt

Vi kan fetmarkera text eller ändra till någon annan tecken vikt med Tailwinds `font-*` klasser för font-weights

| class             | font-weight |
| ----------------- | ----------: |
| `font-thin`       |         100 |
| `font-extralight` |         200 |
| `font-light`      |         300 |
| `font-normal`     |         400 |
| `font-medium`     |         500 |
| `font-semibold`   |         600 |
| `font-bold`       |         700 |
| `font-extrabold`  |         800 |
| `font-black`      |         900 |

[Läs mer om klasser för textstorlekar](https://tailwindcss.com/docs/font-weight)

### Färger

Tailwind ger oss tillgång till en lång lista med färg-skalor med alternativ från `50 -> 950`. Dessa färger kan vi använda med hjälp av olika klasser för text-färg, bakgrunds-färg, border-färg etc.

Vill vi till exempel ha en grön textfärg med Tailwinds `emerald-500` färg kan vi skriva `text-emerald-500`

```html
<p class="text-emerald-500">En grön text</p>
```

| class              | css                       | beskrivning         |
| ------------------ | ------------------------- | ------------------- |
| `text-emerald-500` | color: #00BC7D            | Grön text-färg      |
| `bg-emerald-500`   | background-color: #00BC7D | Grön bakgrunds-färg |
| `border-rose-500`  | border-color: ##FF2056    | Röd border-färg     |

[Här hittar ni en lista med alla Tailwind-färger](https://tailwindcss.com/docs/colors)

### Padding

Tailwind ger oss massor av användbara hjälp-klasser för paddings.

De finns i flera versioner och används tillsammans med en siffra för att välja storlek.
Siffran kan ni multiplicera med `4` så vet ni motsvarande pixel-värde.

Tex: `p-6` motsvarar `padding: 24px`

| padding-class | exempel | Beskrivning                                     |
| ------------- | ------- | ----------------------------------------------- |
| `p-*`         | `p-6`   | Samma padding på alla sidor                     |
| `px-*`        | `px-6`  | Samma padding till vänster och höger - (sidled) |
| `py-*`        | `py-6`  | Samma padding i top och botten - (höjdled)      |
| `pl-*`        | `pl-6`  | Vänster-padding                                 |
| `pr-*`        | `pr-6`  | Höger-padding                                   |
| `pt-*`        | `pt-6`  | Top-padding                                     |
| `pb-*`        | `pb-6`  | Botten-padding                                  |

| class       | Beskrivning                                    |
| ----------- | ---------------------------------------------- |
| `p-0`       | Ta bort all padding                            |
| `px-4 py-6` | 16px padding i sidled & 24px padding i höjdled |

[Läs mer om Tailwinds padding-klasser](https://tailwindcss.com/docs/padding#basic-example)

### Border

Med hjälp av `border` klassen kan vi lägga till en border på ett element

```html
<li class="p-6 border">
  <!-- innehåll här -->
</li>
```

[Läs mer om Tailwinds border klasser här](https://tailwindcss.com/docs/border-color#basic-example)

### Flexbox

Tailwind ger oss små klasser för att enkelt använda `flexbox`. Här nedan ser vi ett exempel på en flexbox med `justify-content: space-between`

```html
<div class="flex justify-between">
  <p>Läs mer</p>
  <div>➡️</div>
</div>
```

| class             | css                              |
| ----------------- | -------------------------------- |
| `flex`            | `display: flex`                  |
| `justify-between` | `justify-content: space-between` |
| `items-center`    | `align-items: center`            |
| `gap-6`           | `gap: 24px`                      |

[Läs mer om Tailwinds flexbox-klasser här](https://tailwindcss.com/docs/flex)

### Hover styling

Med hjälp av ett litet prefix på en tailwind-klass kan vi ställa in att den klassen enbart ska gälla vid tex. hover

Genom att skriva `hover:` innan en tailwind-klass appliceras bara den stylingen vid hover.

> OBS! det kan inte vara något mellanrum mellan `hover:` och den klass du vill använda, de måste skrivas ihop tex: `hover:text-blue-500`

```html
<p class="hover:text-red-500">Den här texten blir röd vid hover</p>
```

[Läs mer om hover, focus och andra states här](https://tailwindcss.com/docs/hover-focus-and-other-states)

### Dark Mode vs Ligt Mode

På samma sätt som vi använde `hover:` här ovanför kan vi använda `dark:` för att säga att en viss klass bara ska gälla i dark mode.

```html
<body class="bg-white text-black dark:bg-black dark:text-white">
  <!-- Innehållet här kommer att ändras vid byte mellan dark/light mode -->
</body>
```

Detta motsvarar att i light mode har bodyn följande:

```html
<body class="bg-white text-black">
  <!-- Innehållet här kommer att ändras vid byte mellan dark/light mode -->
</body>
```

Medans i dark mode har den följande (omvända färger)

```html
<body class="bg-black text-white">
  <!-- Innehållet här kommer att ändras vid byte mellan dark/light mode -->
</body>
```

[Läs mer om `dark:` här](https://tailwindcss.com/docs/dark-mode)

## VS Code Extensions

### Auto-complete för Tailwind-klasser

I denna map hittar vi även [`tailwind.config.ts`](/tailwind.config.ts) filen som enbart finns med för att vi ska kunna använda VS Code Extension:en [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)

### Brusigt med många klasser?

För de som vill kan en till VS Code Extension vara hjälpsam för att tillfälligt visa/dölja alla Tailwind-klasser som snabbt kan bli många och göra det lite svårare att överblicka koden:
[Tailwind Fold](https://marketplace.visualstudio.com/items?itemName=stivo.tailwind-fold)
