### @activities true

# Lag et spill om miljøet i havet
## Introduksjon
### Havet @unplugged
Over 70 prosent av overflaten til jorda er dekket av hav.
Havet er viktig for alt liv på jorda.
For eksempel er regnet som faller fra skyene havvann som har fordampet, og over halvparten av oksygenet vi puster inn kommer fra alger i havet.
Her kan du lage et spill som handler om hvordan vi kan ta vare på havene våre.

### Steg 1 Velg en bakgrunnsfarge
Det første du må gjøre er å lage en verden som spillet ditt kan foregå i.
Siden spillet skal handle om havet, er det fint å finne en bakgrunnsfarge som kan minne om vann.
Hent en ``||scene:set background color to||``-blokk fra ``||scene:Scene||``-menyen og legg den inn i gapet på den grønne ``||loops:on start||``-blokka.
Klikk på det ovale feltet i ``||scene:set background color to||``-blokken og velg den lyseblå fargen.
Du kan trykke på lyspæren for å se hvordan koden skal se ut.
Klikk ``||scene:Next||`` for å gå videre når du er ferdig.

```blocks
// @highlight
scene.setBackgroundColor(9)
```

### Steg 2 Begynn å lage en øy
Verden består ikke bare av hav, den består også av landjord. I de neste trinnene skal du lage en øy i havet.
Start med å hente en ``||scene:set tilemap to||``-blokk fra ``||scene:Scene||``-menyen og sett den inn i koden din under ``||scene:set background color to||``-blokken.

```blocks
scene.setBackgroundColor(9)
// @highlight
tiles.setCurrentTilemap(tilemap`level1`)
```

### Steg 3 Bestem størrelsen på spillbrettet
Klikk på det grå kvadratet i ``||scene:set tilemap to||``-blokken.
Da åpnes verktøyvinduet du bruker til å redigere kartet over spillverdenen din.
Du kan endre størrelsen ved å endre på tallene nede i venstre hjørne av vinduet.
Klikk på hvert av de to tallene og endre dem så det står 32 og 32 der det stod 16 og 16.
Klikk på ``||loops:Done||`` nede i høyre hjørne av verkstøyvinduet når du er ferdig.

![Brettstørrelse](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Drawislandsize.jpg)
![32 x 32](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Drawislandsize002.jpg)

### Steg 4 Tegn en øy
Spillbrettet er delt inn i kvadrater som kalles tiles på engelsk, eller fliser på norsk.
Klikk på det grå kvadratet i ``||scene:set tilemap to||``-blokken på nytt.
Pass på at blyantverktøyet er valgt. Du finner det rett under det grå kvadratet på venstre side i vinduet.
Velg den sandfargede flisen på venstre side i vinduet og tegn omrisset av en øy i det store kvadratet midt på skjermen.
Pass på at omrisset med sandfliser er tett.

![Island](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Island001.jpg)

### Steg 5 Tegn en øy - del 2
Nå har du tegnet sandstranden rundt øya. Da gjenstår det bare å fylle den med gress!
Velg bøtteverktøyet under det grå kvadratet på venstre side, og en gressfarget flis.
Når du har gjort det, klikker du midt inne i omrisset av øya, så den fylles med gressfliser.
Etter det kan du gå over med blyantverktøyet og legge til detaljer som du vil.
