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
Ikke glem å trykke på ``||loops:Done||`` nede i høyre hjørne når du er fornøyd!
Klikk på lyspæren for å se hvor du finner bøtteverktøyet.

![Gressflis og bøtteverktøy](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Islandbucket.jpg)

### Steg 6 Lag en spillfigur
Nå trenger du en spillfigur som du kan kontrollere.
Hent blokken ``||variables:set mySprite to sprite of kind Player||`` fra ``||sprites:Sprites||``-menyen og legg den inn under ``||scene:set tilemap to||``-blokken i koden din.

```blocks
scene.setBackgroundColor(9)
tiles.setTilemap(tiles.createTilemap(hex`2000200000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000001010100000000000000000000000000000000000000000000000000000001010101010101010000000000000000000000000000000000000000000001010101010101010101010101000000000000000000000000000000000001010102020202020202020202020100000000000000000000000000000000010102020202020202020202020202010100000000000000000000000000000001020202020202020202020202020201000000000000000000000000000000010102020202020202020202020202020100000000000000000000000000000001020202020202020202020202020201010000000000000000000000000000000102020202020202020202020202010100000000000000000000000000000000010202020202020202020202020101000000000000000000000000000000000001020202020202020202020201010000000000000000000000000000000000000101020202020202020202020100000000000000000000000000000000000000000102020202020202020202010000000000000000000000000000000000000000010102020202020202020201010000000000000000000000000000000000000000010102020202020202020201000000000000000000000000000000000000000000010102020202020202020100000000000000000000000000000000000000000000010102020202020202010000000000000000000000000000000000000000000000010102020202020201000000000000000000000000000000000000000000000000010101020202010100000000000000000000000000000000000000000000000000000101010101000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000`, img`
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
................................
`, [myTiles.transparency16, sprites.castle.tilePath5, sprites.castle.tileGrass1], TileScale.Sixteen))
// @highlight
let mySprite = sprites.create(img`
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    . . . . . . . . . . . . . . . . 
    `, SpriteKind.Player)
```

### Steg 7 Lag en spillfigur - Del 2
Klikk på det grå kvadratet i ``||variables:set mySprite to sprite of kind Player||``-blokken for å åpne sprite-editoren.
Her kan du enten tegne din egen spillfigur, eller du kan klikke på "Gallery" på linjen øverst i vinduet og velge deg en av figurene du finner der.

![Galleri](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/SpriteGallery.jpg)

### Steg 8 Lag en spillfigur - Del 3
Nå kan du se spillfiguren din på det lille spillkonsollet når du starter spillet, men kanskje den dukker opp midt ute i havet?.
Spillfiguren skal starte spillet på øya, og til det trenger du en spesiell blokk.
Hent blokken ``||scene:place mySprite on top of random||`` fra ``||scene:Scene||``-menyen, og plasser den nedesrt i koden din.
Klikk på det grå kvadratet på blokken, og velg det gressfargede kvadratet fra menyen som dukker opp.

```blocks
scene.setBackgroundColor(9)
tiles.setTilemap(tilemap`level2`)
let mySprite = sprites.create(img`
    . . . . . f f 4 4 f f . . . . . 
    . . . . f 5 4 5 5 4 5 f . . . . 
    . . . f e 4 5 5 5 5 4 e f . . . 
    . . f b 3 e 4 4 4 4 e 3 b f . . 
    . . f 3 3 3 3 3 3 3 3 3 3 f . . 
    . f 3 3 e b 3 e e 3 b e 3 3 f . 
    . f 3 3 f f e e e e f f 3 3 f . 
    . f b b f b f e e f b f b b f . 
    . f b b e 1 f 4 4 f 1 e b b f . 
    f f b b f 4 4 4 4 4 4 f b b f f 
    f b b f f f e e e e f f f b b f 
    . f e e f b d d d d b f e e f . 
    . . e 4 c d d d d d d c 4 e . . 
    . . e f b d b d b d b b f e . . 
    . . . f f 1 d 1 d 1 d f f . . . 
    . . . . . f f b b f f . . . . . 
    `, SpriteKind.Player)
// @highlight
tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
```

### Steg 9 Lag en spillfigur - Del 4
Forsvant spillfiguren din da spillet startet igjen?
For at spillfiguren din alltid skal holde seg synlig i spillet, må du hente blokken ``||scene:camera follow sprite mySprite||`` fra ``||scene:Scene-menyen||``.
Legg den inn nederst i koden din. Sjekk om du kan se spillfiguren når spillet starter på nytt.

```blocks
scene.setBackgroundColor(9)
tiles.setTilemap(tilemap`level2`)
let mySprite = sprites.create(img`
    . . . . . f f 4 4 f f . . . . . 
    . . . . f 5 4 5 5 4 5 f . . . . 
    . . . f e 4 5 5 5 5 4 e f . . . 
    . . f b 3 e 4 4 4 4 e 3 b f . . 
    . . f 3 3 3 3 3 3 3 3 3 3 f . . 
    . f 3 3 e b 3 e e 3 b e 3 3 f . 
    . f 3 3 f f e e e e f f 3 3 f . 
    . f b b f b f e e f b f b b f . 
    . f b b e 1 f 4 4 f 1 e b b f . 
    f f b b f 4 4 4 4 4 4 f b b f f 
    f b b f f f e e e e f f f b b f 
    . f e e f b d d d d b f e e f . 
    . . e 4 c d d d d d d c 4 e . . 
    . . e f b d b d b d b b f e . . 
    . . . f f 1 d 1 d 1 d f f . . . 
    . . . . . f f b b f f . . . . . 
    `, SpriteKind.Player)
tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
// @highlight
scene.cameraFollowSprite(mySprite)
```

### Steg 10 Lage en spillfigur - Del 5
Spillfiguren din skal nå havne på en tilfeldig gressfarget flis hver gang spillet starter.
Du kan trykke på knappen med to piler som går rundt hverandre under spillskjermen for å starte spillet på nytt flere ganger.
Da kan du sjekke at figuren din starter på forskjellige steder hver gang.

![Refresh](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Refresh.jpg)

### Steg 11 Styre spillfiguren
For å kunne bevege spillfiguren din rundt i spillet trenger du blokken ``||controller:move mySprite with buttons||``.
Hent den fra ``||controller:Controller||``-menyen og legg den inn nederst i koden din.
Nå kan du styre spillfiguren din rundt på skjermen. Test litt før du går videre.

```blocks
scene.setBackgroundColor(9)
tiles.setTilemap(tilemap`level2`)
let mySprite = sprites.create(img`
    . . . . . f f 4 4 f f . . . . . 
    . . . . f 5 4 5 5 4 5 f . . . . 
    . . . f e 4 5 5 5 5 4 e f . . . 
    . . f b 3 e 4 4 4 4 e 3 b f . . 
    . . f 3 3 3 3 3 3 3 3 3 3 f . . 
    . f 3 3 e b 3 e e 3 b e 3 3 f . 
    . f 3 3 f f e e e e f f 3 3 f . 
    . f b b f b f e e f b f b b f . 
    . f b b e 1 f 4 4 f 1 e b b f . 
    f f b b f 4 4 4 4 4 4 f b b f f 
    f b b f f f e e e e f f f b b f 
    . f e e f b d d d d b f e e f . 
    . . e 4 c d d d d d d c 4 e . . 
    . . e f b d b d b d b b f e . . 
    . . . f f 1 d 1 d 1 d f f . . . 
    . . . . . f f b b f f . . . . . 
    `, SpriteKind.Player)
tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
scene.cameraFollowSprite(mySprite)
// @highlight
controller.moveSprite(mySprite)
```

### Mikroplast @unplugged
Den første oppgaven til spillfiguren blir å fjerne mikroplast fra havet rundt øya.
Mikroplast er et økende problem i havet, og utgjør en stadig større trussel for alt som lever der.
Å fjerne plast fra havet er derfor en viktig oppgave.
Mikroplasten skal være en ny sprite, men du må ha mange kopier av den.
Derfor skal koden for mikroplasten ligge i en løkke, eller loop, som det heter på kodespråket.

### Steg 12 Lag en løkke
Hent en ``||loops:repeat 4 times||``-blokk fra ``||loops:Loops||``-menyen og sett den inn nederst i koden din.
Endre tallet 4 til 25 ved å klikke på den hvite ovalen og skrive inn tallet 25.

```blocks
scene.setBackgroundColor(9)
tiles.setTilemap(tilemap`level2`)
let mySprite = sprites.create(img`
    . . . . . f f 4 4 f f . . . . . 
    . . . . f 5 4 5 5 4 5 f . . . . 
    . . . f e 4 5 5 5 5 4 e f . . . 
    . . f b 3 e 4 4 4 4 e 3 b f . . 
    . . f 3 3 3 3 3 3 3 3 3 3 f . . 
    . f 3 3 e b 3 e e 3 b e 3 3 f . 
    . f 3 3 f f e e e e f f 3 3 f . 
    . f b b f b f e e f b f b b f . 
    . f b b e 1 f 4 4 f 1 e b b f . 
    f f b b f 4 4 4 4 4 4 f b b f f 
    f b b f f f e e e e f f f b b f 
    . f e e f b d d d d b f e e f . 
    . . e 4 c d d d d d d c 4 e . . 
    . . e f b d b d b d b b f e . . 
    . . . f f 1 d 1 d 1 d f f . . . 
    . . . . . f f b b f f . . . . . 
    `, SpriteKind.Player)
tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
scene.cameraFollowSprite(mySprite)
controller.moveSprite(mySprite)
// @highlight
for (let index = 0; index < 25; index++) {
	
}
```

### Steg 13 Lag en mikroplastsprite
Nå trenger du en ``||variables:set mySprite2 to sprite of kind Player||``-blokk fra ``||sprites:Sprites||``-menyen.
Legg den inn i gapet på ``||loops:repeat 25 times||``-blokken.

```blocks
let mySprite2: Sprite = null
scene.setBackgroundColor(9)
tiles.setTilemap(tilemap`level2`)
let mySprite = sprites.create(img`
    . . . . . f f 4 4 f f . . . . . 
    . . . . f 5 4 5 5 4 5 f . . . . 
    . . . f e 4 5 5 5 5 4 e f . . . 
    . . f b 3 e 4 4 4 4 e 3 b f . . 
    . . f 3 3 3 3 3 3 3 3 3 3 f . . 
    . f 3 3 e b 3 e e 3 b e 3 3 f . 
    . f 3 3 f f e e e e f f 3 3 f . 
    . f b b f b f e e f b f b b f . 
    . f b b e 1 f 4 4 f 1 e b b f . 
    f f b b f 4 4 4 4 4 4 f b b f f 
    f b b f f f e e e e f f f b b f 
    . f e e f b d d d d b f e e f . 
    . . e 4 c d d d d d d c 4 e . . 
    . . e f b d b d b d b b f e . . 
    . . . f f 1 d 1 d 1 d f f . . . 
    . . . . . f f b b f f . . . . . 
    `, SpriteKind.Player)
tiles.placeOnRandomTile(mySprite, sprites.castle.tileGrass1)
scene.cameraFollowSprite(mySprite)
controller.moveSprite(mySprite)
for (let index = 0; index < 4; index++) {
    mySprite2 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Player)
}
```

### Mikroplast Del 2 @unplugged
Plast råtner ikke, men når den blir liggende i naturen brytes den ned til stadig mindre plastbiter.
Mikroplast er plastbiter som er mindre enn 5 millimeter store.
Biter av plast kan likne på mat, sånn at dyr spiser den.
Noen plastbiter er til og med så små at dyreplankton kans spise dem.
Når større dyr spiser dyreplankton med mikroplast i seg, får de også i seg plast.
Dyrene kan ikke fordøye plasten, men den kan bli værende i kroppen deres og gjøre skade.
Man har gjort funn av både fugler og delfiner med magen så full av plast at de ikke får i seg mat.
Derfor må plasten bort fra havet.


<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>