### @explicitHints false

## Introduksjon @unplugged
Her vil du lære å kode våre kule LED displayer. Ved å sette på en LED og velge farge!

## Steg 1: Definer noen neopixler @fullscreen
 Trykk på ``||Neopixel: Neopixel||`` fra blokkmenyen.
 Klikk og dra inn blokken ``||Neopixel: sett strip til ||`` og slipp den inn i ``||basic: ved start ||`` blokken.
 Velg pinne ``||Neopixel: P0||`` og antall LED til ``||Neopixel: 768||`` la format stå som ``||Neopixel: RGB (GRB) ||``.
 Denne blokken brukes for å velge hvilken pinne som er koblet til LED, hvor mange LEDèr det er og hvilken type LED. 

```blocks

let strip = neopixel.create(DigitalPin.P0, 768, NeoPixelMode.RGB)

```
## Steg 2: Slette minne i LED
Trykk på ``||Neopixel: Neopixel ||`` fra blokkmenyen.
Klikk og dra inn blokken ``||Neopixel: strip.clear ||`` plasser den under forrige blokk.
Denne blokken sletter tidligere data inni lysdidodene.

```blocks

let strip = neopixel.create(DigitalPin.P0, 768, NeoPixelMode.RGB)
strip.clear()

```

## Steg 3: Velge hvilken lysdidoe som skal lyse og hvilken farge

Trykk på ``||Neopixel: Neopixel||`` fra blokkmenyen og klikk deretter ``||Neopixel: mer ||``.
Klikk og dra inn blokken ``||Neopixel: strip set_Pixel_Color at 0 to Red ||`` plasser den nederst. 
Denne blokken brukes for å velge hvilken LED som skal lyse (0-767) og hvilken farge.

```blocks

let strip = neopixel.create(DigitalPin.P0, 768, NeoPixelMode.RGB)
strip.clear()
strip.setPixelColor(0, neopixel.colors(NeoPixelColors.Red))

```

## Steg 3: Send informasjon til Neopixlene
Trykk på ``||Neopixel: Neopixel ||`` fra blokkmenyen.
Klikk og dra inn blokken ``||Neopixel: strip.show||`` plasser den nederst.
Denne blokken sender hvilken LED nummer og farge til LEDène som skal lyse.

```blocks

let strip = neopixel.create(DigitalPin.P0, 768, NeoPixelMode.RGB)
strip.clear()
strip.setPixelColor(0, neopixel.colors(NeoPixelColors.Red))
strip.show()

```

## Steg 4 Leste ned på microbiten

hvis du har en @boardname@ tilkoblet, trykk ``|last ned|``!
Prøv nå også endre farge og hvilken LED som skal lyse for så å trykke ``|last ned|`` igjen.
For hver endring vi gjør i koden må det lastes ned på nytt til @boardname@.
