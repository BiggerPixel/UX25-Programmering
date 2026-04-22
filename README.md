# Programmering för UX-Produktion 2026

# Dag 3 - Samanfattning

Under lektion 3 återskapade vi en meny från en sida på nätet och kikade även på några nya CSS-features.

### Hover-states

CSS-Variabler fungerar väldigt likt variabler i Figma. De underlättar för oss genom att vi kan samla många användningar av ett värde på ett ställe och därmed lättare göra ändringar.

```css
/* Såhär skapar vi CSS-variabler */
:root {
  --menu-bg: #102442;
  --color-menu-link: white;
  --color-menu-link-hover: #5a90e0;
}
```

```css
/* Såhär använder vi en CSS-variabel */
.main-menu {
  background-color: var(--menu-bg);
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
