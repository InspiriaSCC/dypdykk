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
scene.setBackgroundColor(9)
```

### Steg 2 Begynn å lage en øy
Verden består ikke bare av hav, den består også av landjord. I de neste trinnene skal du lage en øy i havet.
Start med å hente en ``||scene:set tilemap to||``-blokk fra ``||scene:Scene||``-menyen og sett den inn i koden din under ``||scene:set background color to||``-blokken.

```blocks
scene.setBackgroundColor(9)
tiles.setCurrentTilemap(tilemap`level1`)
```

### Steg 3 Bestem størrelsen på spillbrettet


