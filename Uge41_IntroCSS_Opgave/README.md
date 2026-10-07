# Uge 41 – Introduktion til CSS: kommentar- og forklaringsopgave

Undervisningsmateriale til Uge 41. Bygger videre på `Uge41_IntroCSS.pptx`
(de tre metoder at indsætte CSS, regler, selektorer, kommentarer) og dækker
desuden CSS Tekst, Font, Liste-visning, Farver og Baggrund.

## Indhold

| Fil | Hvad er det |
|---|---|
| `Opgave_Uge41_IntroCSS.docx` | Opgaveark til eleverne (5 sider, A4) |
| `Facit_Uge41_IntroCSS.docx` | Vejledende svar til læreren (6 sider, A4) |
| `elev/` | Startfiler til eleverne – CSS uden kommentarer |
| `facit/` | Samme filer med kommentarer og forklaringer |

Begge mapper indeholder `index.html`, `css/style.css` og `img/` (to SVG-filer).
`elev/` og `facit/` er identiske bortset fra kommentarerne, så elevens
kommenterede fil kan sammenlignes direkte med facit.

## Sådan bruges det

Eleverne åbner `elev/index.html` i browseren og mappen i deres editor.
De skal ikke ændre designet i del 1–4 – kun tilføje kommentarer og svare
på spørgsmålene. Del 5 er eksperimenter, hvor de gerne må ændre koden.

## Bevidste konflikter i koden (kernen i opgaven)

Koden er sat sammen, så fire konflikter kan iagttages direkte:

1. **Inline vs. stylesheet** – `<section>` har `style="border-left: 6px solid #e63946;"`
   mens `.kort` sætter `border-left: 6px solid #cccccc`. Inline vinder → kanten er rød.
2. **id vs. klasse** – `.kort` sætter `background-color: #f0f0f0` og `#kort` sætter
   `#ffffff`. Id vinder → kortet er hvidt.
3. **Rækkefølge ved lige specificitet** – `<style>` står før `<link>`, og begge sætter
   `background-color` på `body` med en elementselektor. Den eksterne fil vinder.
   Flytter man `<link>` op, skifter baggrunden (opgave 1d).
4. **list-style-image vs. list-style-type** – begge er sat på `.kompetencer`.
   Billedet vinder → man ser det røde punkt, ikke firkanterne.

Alle fire er synlige i Chrome DevTools, hvor de tabende declarations står streget over.
