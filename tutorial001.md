### @activities true

# Dypdykk: Lag et spill om miljøet i havet
## Introduksjon
### Dypdykk @unplugged
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

### Steg 4 Tegn en øy - Del 1
Spillbrettet er delt inn i kvadrater som kalles tiles på engelsk, eller fliser på norsk.
Klikk på det grå kvadratet i ``||scene:set tilemap to||``-blokken på nytt.
Pass på at blyantverktøyet er valgt. Du finner det rett under det grå kvadratet på venstre side i vinduet.
Velg den sandfargede flisen på venstre side i vinduet og tegn omrisset av en øy i det store kvadratet midt på skjermen.
Pass på at omrisset med sandfliser er tett.

![Island](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Island001.jpg)

### Steg 5 Tegn en øy - Del 2
Nå har du tegnet sandstranden rundt øya. Da gjenstår det bare å fylle den med gress!
Velg bøtteverktøyet under det grå kvadratet på venstre side, og en gressfarget flis.
Når du har gjort det, klikker du midt inne i omrisset av øya, så den fylles med gressfliser.
Etter det kan du gå over med blyantverktøyet og legge til detaljer som du vil.
Ikke glem å trykke på ``||loops:Done||`` nede i høyre hjørne når du er fornøyd!
Klikk på lyspæren for å se hvor du finner bøtteverktøyet.

![Gressflis og bøtteverktøy](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Islandbucket.jpg)

### Steg 6 Lag en spillfigur - Del 1
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
Endre typen sprite til ``||sprites:Food||`` ved å klikke på ordet ``||sprites:Player||`` sist i ``||variables:set mySprite2 to sprite of kind Player||``-blokken og så klikke på ordet ``||sprites:Food||`` i menyen som dukker opp.

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
    // @highlight
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
        `, SpriteKind.Food)
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

### Steg 14 Tegn din egen mikroplastsprite
Klikk på det grå kvadratet for å åpne sprite-editoren, og tegn mikroplast ved å lage tilfeldige mønstre av små prikker og streker i sterke farger.
Husk å bruke farger som vil synes mot den blå havbakgrunnen i spillet.
Klikk på ``||loops:Done||`` nede i høyre hjørne når du er fornøyd.

![Mikroplast](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Mikroplast.jpg)

### Steg 15 Plasser mikroplasten tilfeldig i havet
Om du tester spillet nå, finner du mikrplast bare ett sted i havet.
For å spre de 25 spritene, må du plassere hver av dem på et tilfeldig sted i havet.
Hent blokken ``||scene:place mySprite on top of random||`` fra ``||scene:Scene||``-menyen og legg den inn nederst i ``||loops:repeat 25 times||``-blokken.
Endre ``||variables:mySprite||`` til ``||variables:mySprite2||`` ved å klikke på ordet og velge ``||variables:mySprite2||`` fra menyen som kommer opp.
La det grårutede kvadratet være slik det er. Da havner mikroplasten din i havet, der det ikke er noen fliser.
Test spillet for sjekke om det nå er mikroplast i havet rundt øya.

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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    // @highlight
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
```

### Steg 16 Fang mikroplasten - Del 1
For å fange mikroplasten trenger du en blokk som heter ``||sprites:on sprite of kind Player overlaps otherSprite of kind Player||``.
Hent den fra ``||sprites:Sprites||``-menyen og legg den ved siden av resten av koden din.

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Player, SpriteKind.Player, function (sprite, otherSprite) {
	
})
```

### Steg 17 Fang mikroplasten - Del 2
Du må gjøre en endring i den siste blokken.
Klikk på det siste stedet det står ``||sprites:Player||`` og velg ``||sprites:Food||`` fra menyen som dukker opp, slik at det står ``||sprites:on sprite of kind Player overlaps otherSprite of kind Food||``.

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	
})
```

### Steg 18 Fang mikroplasten - Del 3
For å få en sprite til å forsvinne fra spillet trenger du blokken ``||sprites:destroy mySprite||``.
Hent den fra ``||sprites:Sprites||``-menyen og legg den inn i ``||sprites:on sprite of kind Player overlaps otherSprite of kind Food||``-blokken.
Om du tester spillet nå, vil du se at spillfiguren din forsvinner når du treffer et sted med mikroplast, men det skal vi fikse i neste steg.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    // @highlight
    sprites.destroy(mySprite)
})
```

### Steg 19 Fang mikroplasten - Del 4
Blokken ``||sprites:on sprite of kind Player overlaps otherSprite of kind Food||`` beskriver en hendelse der en sprite av typen ``||sprites:Player||`` overlapper en annen sprite av typen ``||sprites:Food||``.
Spillfiguren din er en ``||variables:sprite||`` av typen ``||sprites:Player||``, mens mikroplasten nå er en ``||variables:otherSprite||`` av typen ``||sprites:Food||``.
Du må altså sørge for at det er ``||variables:otherSprite||`` som blir fjernet.
Klikk på det ovale feltet der det står ``||variables:otherSprite||`` og dra ``||variables:otherSprite||`` ned i ovalen i ``||sprites:destroy mySprite||`` der det står ``||variables:otherSprite||``, slik at det står ``||sprites:destroy otherSprite||`` der.
Test spillet og sjekk at mikroplasten blir borte.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    // @highlight
    sprites.destroy(otherSprite)
})
```

### Steg 20 Få poeng
For å få poeng må du bruke blokken ``||info:change score by 1||``.
Hent ``||info:change score by 1||`` fra ``||info:Info||``-menyen og legg den inn i ``||sprites:on sprite of kind Player overlaps otherSprite of kind Food||``-blokken sammen med ``||sprites:destroy otherSprite||``.
Test spillet. Klarer du å finne alle 25 mikroplastfeltene?

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    sprites.destroy(otherSprite)
    // @highlight
    info.changeScoreBy(1)
})
```

### Fremmede arter @unplugged
En fremmed art, eller invaderende art, er en art som blir funnet der den egentlig ikke hører hjemme.
I havet kan fremmede arter komme med havstrømmer eller skipstrafikk.
I Norge har vi nå mange arter som ikke fantes her tidligere: Stillehavsøsters, kongekrabbe, amerikansk hummer, japansk drivtang, havnespy, amerikansk lobemanet og rombekrabbe er noen eksempler.
At nye arter kommer til et område, kan skape problemer for dyrene som allerede lever der.
Nå skal du lage en invaderende type krabbe og forsøke å fange den.

### Steg 21 Lag en fremmed art
Havet rundt øya er blitt infisert av kongekrabber som ødelegger økosystemet.
For å lage mange kongekrabber trenger du en ny løkke.
Hent en ``||loops:repeat 4 times||``-blokk fra ``||loops:Loops||``-menyen og legg den inn nederst i ``||loops:on start||``-hovedkoden din.
Endre tallet 4 til 25.

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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
// @highlight
for (let index = 0; index < 25; index++) {
}
```

### Steg 22 Lag en krabbesprite
Hent en ``||variables:set mySprite3 to sprite of kind Player||``-blokk fra ``||sprites:Sprites||``-menyen og legg den inn i den nye ``||loops:repeat 4 times||``-blokken.
Klikk på ordet ``||sprites:Player||`` og velg ``||sprites:Enemy||`` fra menyen som popper opp.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    // @highlight
    mySprite3 = sprites.create(img`
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
        `, SpriteKind.Enemy)
}
```

### Steg 23 Tegn en krabbe
Klikk på det grå kvadratet i ``||variables:set mySprite3 to sprite of kind Enemy||``-blokken for å åpne sprite-editoren.
Tegn en kongekrabbe! Du kan klikke på lyspæren for å se et eksempel på hvordan en krabbe kan se ut.

![Kongekrabbe](https://raw.githubusercontent.com/InspiriaSCC/dypdykk/master/assets/Kongekrabbe.jpg)

### Steg 24 Plasser kongekrabbene tilfeldig
Hent en ``||scene:place mySprite on top of random||`` fra ``||scene:Scene||``-menyen og endre ``||variables:mySprite||`` til ``||variables:mySprite3||`` ved å klikke på ordet og velge ``||variables:mySprite3||`` fra menyen.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    mySprite3 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . 3 3 . . . . . . . . . . 3 3 . 
        3 . . 3 . . . . . . . . 3 . . 3 
        . . 3 . 3 . 3 3 3 3 . 3 . 3 . . 
        . 3 . . . 3 3 3 3 3 3 . . . 3 . 
        3 . . 3 3 1 f 3 3 1 f 3 3 . . 3 
        . . 3 . 3 3 3 3 3 3 3 3 . 3 . . 
        . 3 . . 3 3 3 3 3 3 3 3 . . 3 . 
        3 . . 3 . 3 . . . . 3 . 3 . . 3 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . 3 . . . 3 b . . b 3 . . . 3 . 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . . . 3 . . . . . . . . 3 . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    // @highlight
    tiles.placeOnRandomTile(mySprite3, assets.tile`transparency16`)
}
```

### Steg 25 Sett krabbene i bevegelse
Hent en ``||sprites:set mySprite velocity to vx 50 vy 50||`` fra ``||sprites:Sprites||``-menyen og endre ``||variables:mySprite||`` til ``||variables:mySprite3||``.
Tallet bak ``||sprites:vx||`` angir farten i høyre-venstre retningen, og tallet etter ``||sprites:vy||`` angir farten i opp-ned retningen. Test spillet og se hva som skjer.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    mySprite3 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . 3 3 . . . . . . . . . . 3 3 . 
        3 . . 3 . . . . . . . . 3 . . 3 
        . . 3 . 3 . 3 3 3 3 . 3 . 3 . . 
        . 3 . . . 3 3 3 3 3 3 . . . 3 . 
        3 . . 3 3 1 f 3 3 1 f 3 3 . . 3 
        . . 3 . 3 3 3 3 3 3 3 3 . 3 . . 
        . 3 . . 3 3 3 3 3 3 3 3 . . 3 . 
        3 . . 3 . 3 . . . . 3 . 3 . . 3 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . 3 . . . 3 b . . b 3 . . . 3 . 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . . . 3 . . . . . . . . 3 . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    tiles.placeOnRandomTile(mySprite3, assets.tile`transparency16`)
    // @highlight
    mySprite3.setVelocity(50, 50)
}
```

### Steg 26 Få krabbene til å sprette tilbake
Som du ser går alle krabben ned mot høyre helt til de treffer utkanten av spillebrettet, og så følger de kanten til alle sitter nede i høyre hjørne.
Hent blokken ``||sprites:set mySprite bounce on wall on||`` fra ``||sprites:Sprites||``-menyen og legge den inn nederst i ``||loops:repeat 25 times||``-løkken der krabbene blir laget.
Endre ``||variables:mySprite||`` til ``||variables:mySprite3||``.
Test spillet og se hva som skjer.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    mySprite3 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . 3 3 . . . . . . . . . . 3 3 . 
        3 . . 3 . . . . . . . . 3 . . 3 
        . . 3 . 3 . 3 3 3 3 . 3 . 3 . . 
        . 3 . . . 3 3 3 3 3 3 . . . 3 . 
        3 . . 3 3 1 f 3 3 1 f 3 3 . . 3 
        . . 3 . 3 3 3 3 3 3 3 3 . 3 . . 
        . 3 . . 3 3 3 3 3 3 3 3 . . 3 . 
        3 . . 3 . 3 . . . . 3 . 3 . . 3 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . 3 . . . 3 b . . b 3 . . . 3 . 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . . . 3 . . . . . . . . 3 . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    tiles.placeOnRandomTile(mySprite3, assets.tile`transparency16`)
    mySprite3.setVelocity(50, 50)
    // @highlight
    mySprite3.setBounceOnWall(true)
}
```

### Steg 27 Gi krabbene tilfeldig fart
For å gjøre spillet mindre forutsigbart kan du bruke en tilfeldighetsfunksjon fra ``||maths:Maths||``-menyen for å oppgi farten til krabbene.
Hent to ovale ``||maths:pick random 0 to 10||``-blokker fra ``||mathc:Maths||``-menyen og sett dem inn i de to hvite feltene der det nå står 50 i ``||sprites:set mySprite3 velocity to vx 50 vy 50||``.
Endre 0 til -50 og 10 til 50 i begge de to ovale blokkene. Test spillet og legg merke til hvordan krabbene beveger seg nå.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    mySprite3 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . 3 3 . . . . . . . . . . 3 3 . 
        3 . . 3 . . . . . . . . 3 . . 3 
        . . 3 . 3 . 3 3 3 3 . 3 . 3 . . 
        . 3 . . . 3 3 3 3 3 3 . . . 3 . 
        3 . . 3 3 1 f 3 3 1 f 3 3 . . 3 
        . . 3 . 3 3 3 3 3 3 3 3 . 3 . . 
        . 3 . . 3 3 3 3 3 3 3 3 . . 3 . 
        3 . . 3 . 3 . . . . 3 . 3 . . 3 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . 3 . . . 3 b . . b 3 . . . 3 . 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . . . 3 . . . . . . . . 3 . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    tiles.placeOnRandomTile(mySprite3, assets.tile`transparency16`)
    // @highlight
    mySprite3.setVelocity(randint(-50, 50), randint(-50, 50))
    mySprite3.setBounceOnWall(true)
}
```

### Fremmede arter - Del 2 @unplugged
En av grunnene til at kongekrabben er fryktet, er at det fort blir mange av dem, og at de nesten støvsuger havbunnen for dyr som lever der.
Kongekrabben spiser muslinger, sjøstjerner, børstemark og rogn fra fisk, og kan etterlate seg områder som nærmest er tømt for liv.
En annen art som lager problemer er stillehavsøsters. Stillehavsøsters formerer seg raskt, og de vokser fort. Det gjør at de dekker store områder der de slår seg ned.
Det blir ikke plass til andre muslingarter, som for eksempel blåskjell. Skallet til stillehavsøstersen er hardt, med skarpe kanter.
Dyr som normalt spiser blåskjell klarer ikke å spise stillehavsøsters, og får problemer med å finne mat der stillehavsøstersen overtar.
Å fjerne fremmedarter kan være en nærmest umulig oppgave. Nå skal du forsøke å fange de vandrende kongekrabbene.

### Steg 28 Fang krabbene - Del 1
Nå trenger du en ny ``||sprites:on sprite of kind Player overlaps otherSprite of kind Player||`` blokk fra ``||sprites:Sprites||``-menyen.
Legg den ved siden av resten av koden din, og endre det siste stedet der det står ``||sprites:Player||`` til ``||sprites:Enemy||``.

```blocks
// @highlight
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
	
})
```

### Steg 29 Fang krabbene - Del 2
Hent en ``||sprites:destroy mySprite||`` fra ``||sprites:Sprite||``-menyen og legg den inn i ``||sprites:on sprite of kind Player overlaps otherSprite of kind Enemy||``-blokken.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    // @highlight
    sprites.destroy(mySprite)
})
```

### Steg 30 Fang krabbene - Del 3
Klikk på ovalen som det står ``||variables:otherSprite||`` på i ``||sprites:on sprite of kind Player overlaps otherSprite of kind Enemy||``-blokken og dra den dit hvor det står ``||variables:mySprite||`` i ``||sprites:destroy mySprite||``-blokken.
Test spillet og sjekk at krabbene blir borte når du tar dem.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    // @highlight
    sprites.destroy(otherSprite)
})
```

### Steg 31 Få poeng for krabbene
Hent en ``||info:change score by 1||``-blokk fra ``||info:Info||``-menyen og plasser under ``||sprites:destroy mySprite||`` i ``||sprites:on sprite of kind Player overlaps otherSprite of kind Enemy||``-blokken.
Test spillet og sjekk at du får poeng når du fanger en krabbe.

```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Enemy, function (sprite, otherSprite) {
    sprites.destroy(otherSprite)
    // @highlight
    info.changeScoreBy(1)
})
```

### Steg 32 Begrens tiden
Nå gjenstår det bare å gjøre spillet litt mer utfordrende.
Hent en ``||info:start countdown||``-blokk fra ``||info:Info||``-menyen og plasser den i hovedkoden din, nederst i ``||loops:on start||``-blokken.
Endre tiden fra 10 sekunder til 30. Test spillet noen ganger. Hva ble high-scoren din? 50 poeng er den høyest mulige poengsummen om du har fulgt instruksjonen til punkt og prikke.

```blocks
let mySprite3: Sprite = null
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
for (let index = 0; index < 25; index++) {
    mySprite2 = sprites.create(img`
        . . . . 8 . . . . . . . . . . . 
        . . . . . 8 . . . . . . . . . . 
        . . . . . . 8 . . . 2 2 . . . . 
        . . . 3 3 . . . . . . . 2 . . . 
        . . 3 . 5 . . . . . . . . . . . 
        . . . 5 . . . . . . . . . . . . 
        . . 5 . . . . . 7 7 . . . . . . 
        . . . . . 5 5 . . . 7 . . . . . 
        . . 8 . . . 5 . . 3 . . . . . . 
        . 8 . . . . . 3 3 . . . a . . . 
        8 . . . 7 . . . . . . a . . . . 
        . . . . 7 . . . . . a . . . . . 
        . . . 7 . . . . . . . . . . . . 
        . . . . . . . 4 . . . . . . . . 
        . . . . . . . . 4 . . . . . . . 
        . . . . . . . . . 4 . . . . . . 
        `, SpriteKind.Food)
    tiles.placeOnRandomTile(mySprite2, assets.tile`transparency16`)
}
for (let index = 0; index < 25; index++) {
    mySprite3 = sprites.create(img`
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        . 3 3 . . . . . . . . . . 3 3 . 
        3 . . 3 . . . . . . . . 3 . . 3 
        . . 3 . 3 . 3 3 3 3 . 3 . 3 . . 
        . 3 . . . 3 3 3 3 3 3 . . . 3 . 
        3 . . 3 3 1 f 3 3 1 f 3 3 . . 3 
        . . 3 . 3 3 3 3 3 3 3 3 . 3 . . 
        . 3 . . 3 3 3 3 3 3 3 3 . . 3 . 
        3 . . 3 . 3 . . . . 3 . 3 . . 3 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . 3 . . . 3 b . . b 3 . . . 3 . 
        . . 3 . . 3 3 . . 3 3 . . 3 . . 
        . . . 3 . . . . . . . . 3 . . . 
        . . . . . . . . . . . . . . . . 
        . . . . . . . . . . . . . . . . 
        `, SpriteKind.Enemy)
    tiles.placeOnRandomTile(mySprite3, assets.tile`transparency16`)
    mySprite3.setVelocity(randint(-50, 50), randint(-50, 50))
    mySprite3.setBounceOnWall(true)
}
// @highlight
info.startCountdown(30)
```

### Steg 33
Gratulerer! Du har kodet et helt spill der du forsøker å bekjempe noen av problemene i havet.
Når du trykker på ``||scene:Done||`` kommer du til å få tilgang til alle kodeblokkene i MakeCode Arcade.
Du kan også velge om du vil dele spillet ditt med andre brukere på MakeCode, slik at de kan spille det.
Og så kan du kanskje bruke det du har lært til å lage flere dyr eller typer forsøpling, og gjøre spillet enda større?

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>