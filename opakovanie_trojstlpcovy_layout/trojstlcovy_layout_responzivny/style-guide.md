# Front-end Style Guide (responzívna verzia)

Toto zadanie nadväzuje na `trojstlcovy_layout`. Pridáva hlavičku s navigáciou, pätu (footer)
a hlavne **responzívny layout**, ktorý sa mení podľa šírky obrazovky.

## Breakpointy (medzné body)

- **Mobil**: do 599px  → 1 stĺpec
- **Tablet**: 600px – 899px → 2 stĺpce
- **Desktop**: od 900px → 3 stĺpce

V CSS použi `@media (min-width: ...)` — vždy stavaj štýly "mobile first"
(najprv základné štýly pre mobil, potom ich cez media queries rozširuješ pre väčšie obrazovky).

## Relatívne jednotky

V tomto zadaní sa vyhýbaj pevným `px` hodnotám všade tam, kde to dáva zmysel:

- `rem` — pre veľkosti písma a odstupy (nezávislé od rodiča, viažu sa na `<html>`)
- `em` — pre veľkosti naviazané na okolitý text
- `%` — pre šírky stĺpcov / kontajnerov
- `vw` / `vh` — pre veľkosti závislé od šírky/výšky okna
- `clamp(min, preferovaná, max)` — pre plynulé škálovanie písma medzi breakpointmi

## Layout

- **Header**: logo + navigácia (na mobile sa položky navigácie zalomia/pod seba)
- **Main**: tri karty (Sedans, SUV, Luxury) v grid layoute — 1 / 2 / 3 stĺpce podľa breakpointu
- **Footer**: tri stĺpce s obsahom (O nás, Kontakt, Sociálne siete) + copyright riadok

## Colors

### Primary

Bright orange: hsl(31, 77%, 52%)      oklch(70.82% 0.1512 61.38)
Dark cyan: hsl(184, 100%, 22%)        oklch(47.37% 0.0807 203.41)
Very dark cyan: hsl(179, 100%, 13%)   oklch(34.38% 0.0589 192.89)

### Neutral

Transparent white (paragraphs): hsla(0, 0%, 100%, 0.75)
Very light gray (background, headings, buttons): hsl(0, 0%, 95%)

## Typography

### Body Copy

- Font size: 15px (základ, ďalej sa škáluje cez rem/clamp)

### Font

- Family: [Lexend Deca](https://fonts.google.com/specimen/Lexend+Deca)
- Weights: 400

- Family: [Big Shoulders Display](https://fonts.google.com/specimen/Big+Shoulders+Display)
- Weights: 700

## Úloha pre žiakov

1. Doplň chýbajúce štýly pre navigáciu tak, aby sa na mobile položky pod sebou nezobrazovali
   nahusto (priprav si vlastný odstup pomocou `rem`/`em`).
2. Uprav `grid-template-columns` v troch breakpointoch tak, aby si videl/videla zmenu na
   `mobile-design.jpg` → tablet → `desktop-design.jpg` (over si to zmenšovaním okna prehliadača).
3. Skús nahradiť aspoň 2 pevné veľkosti písma za `clamp()`.
4. V päte uprav rozostupy stĺpcov pomocou `gap` v `rem`.
