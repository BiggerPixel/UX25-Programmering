# Programmering för UX-Produktion 2026

## Lektion 6

Under lektion 6 kikade vi på hur man bygger formulär i HTML och pratade även om varför det är viktigt att välja rätt formulärelement för att skapa en bra UX.

Vi gick igenom några vanliga formulär-element och tittade på hur de används för att samla in olika typer av information från användaren. Vi pratade också om att HTML redan från början har många smarta funktioner inbyggda, tex. att vi kan välja olika typer av input beroende på vad användaren ska skriva in.

## Vi har under lektionen:

- Kikat på hur man bygger formulär i HTML
- Gått igenom vanliga formulär-element
- Pratat om vikten av att välja rätt formulärelement för rätt typ av innehåll
- Kikat på hur rätt val av element kan förbättra UX
- Byggt ett enkelt formulär med e-post, lösenord och meddelande
- Använt labels, inputs, textarea och button

## Formulär i HTML

För att skapa ett formulär använder vi elementet `<form>`. Det används för att samla ihop fält där användaren kan skriva eller välja information och sedan skicka in den.

```html
<form></form>
```

## Fieldset

Vi använde också `<fieldset>` för att gruppera ihop formulärets olika delar.

```html
<fieldset></fieldset>
```

Detta är ett grupperande element för formulär och gör strukturen tydligare.

## Label

`<label>` används för att beskriva vad ett fält är till för. Det är viktigt både för tydlighet, UX och tillgänglighet.

```html
<label for="email">E-post</label>
```

Attributet `for` kopplas till ett `id` på input-fältet. På så sätt hör labeln ihop med rätt fält.

## Input

`<input>` används när användaren ska skriva in kortare information, tex. e-post eller lösenord.

### Input type email

```html
<input id="email" type="email" placeholder="john.doe@example.com" required />
```

När vi använder `type="email"` hjälper webbläsaren oss att förstå att fältet är till för en e-postadress. Det kan tex. ge bättre validering och i vissa fall rätt tangentbord på mobil.

### Input type password

```html
<input id="password" type="password" placeholder="Skriv ditt lösenord här..." />
```

När vi använder `type="password"` döljs tecknen som skrivs in i fältet.

## Textarea

`<textarea>` används när användaren ska skriva längre text, tex. ett meddelande.

```html
<textarea id="message" placeholder="Skriv ett emddelande här..."></textarea>
```

Detta är ett bättre val än ett vanligt input-fält när innehållet förväntas vara längre.

## Button

Vi använde även en knapp för att skicka formuläret.

```html
<button type="submit">Skicka</button>
```

`type="submit"` betyder att knappen används för att skicka formuläret.

## Placeholder

Vi använde attributet `placeholder` i flera fält.

```html
placeholder="john.doe@example.com"
```

Placeholder används för att visa ett exempel eller en hint inne i fältet innan användaren börjar skriva. En placeholder ska aldrig användas itsället för en label. Det leder annars till accessibillity-issues och dålig UX då placeholder-texten försvinner så fort användaren börjat fylla i fältet.

## Required

Vi använde även attributet `required`.

```html
required
```

Det betyder att fältet måste fyllas i innan formuläret kan skickas.

## Viktigt för UX

En viktig del av lektionen var att rätt formulärelement ger bättre UX.

Tex:

- använd `type="email"` för e-post
- använd `type="password"` för lösenord
- använd `<textarea>` för längre meddelanden
- använd `<label>` så att användaren tydligt förstår vad varje fält är till för

Om vi väljer rätt element från början blir formuläret tydligare, enklare att använda och ofta också mer tillgängligt.

## Exempel på formuläret vi byggde

```html
<form>
  <fieldset>
    <label for="email">E-post</label>
    <input
      id="email"
      type="email"
      placeholder="john.doe@example.com"
      required
    />
  </fieldset>

  <fieldset>
    <label for="password">Lösenord</label>
    <input
      id="password"
      type="password"
      placeholder="Skriv ditt lösenord här..."
    />
  </fieldset>

  <fieldset>
    <label for="message">Meddelande</label>
    <textarea id="message" placeholder="Skriv ett emddelande här..."></textarea>
  </fieldset>

  <button type="submit">Skicka</button>
</form>
```
