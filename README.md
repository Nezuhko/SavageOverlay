# Savage Overlay

Overlay grafico Ki per Minecraft Java 1.8 / SavageMC KitOP.

## Download

[Scarica SavageOverlay-1.8.zip](https://github.com/Nezuhko/SavageOverlay/releases/download/v1.0.0/SavageOverlay-1.8.zip)

La release contiene lo ZIP del resource pack e il relativo SHA-256.
`pack.mcmeta` e' alla radice dello ZIP; formato pack 1, tre risorse complessive.

## Grafica

Barra XP bianca con contorno argento e canale scuro. La logica e i punti del Ki
sono gestiti dal Core separato; questa distribuzione contiene soltanto la grafica.

Minecraft 1.8 sostituisce l'intero foglio `textures/gui/icons.png`: questa variante
usa le altre icone vanilla. Blocchi, armi, cielo e altre risorse non sono inclusi.
Per preservare cuori e altre icone HUD di una pack personalizzata occorre generare
una variante a partire dal suo foglio icone. Non e' un adattamento universale.

## Collegamento al Core

In `plugins/SavageCoreKitOP/overlay.yml`, impostare `pack.url` al link diretto
del download sopra e mantenere `http.enabled: false` per l'hosting tramite GitHub.
Usare `/overlay reload`, poi `/overlay riprova` o rientrare nel server.

La compatibilita' visiva con Lunar in gioco e' ancora da verificare.

## Variante opzionale: seconda barra Ki

[SavageOverlay-KiBossBar-1.8.zip](https://github.com/Nezuhko/SavageOverlay/releases/download/v1.0.0/SavageOverlay-KiBossBar-1.8.zip) rende bianca anche la
barra boss superiore, oltre alla XP. E' una variante per la prova sperimentale
del Core: non introduce una HUD posizionabile liberamente.

Il pack da solo non attiva la seconda barra. Sul Core occorre abilitare
`ki.experimental-bossbar: true` in overlay.yml, usare `/overlay reload` e
selezionare `/overlay ki bossbar` sul proprio giocatore. La barra usa ancora le
condizioni del Ki: Survival/Adventure, combat tag attivo, niente duello gestito
da un sistema esterno. La scelta personale si azzera al rientro.

La prova visiva Lunar resta da eseguire. La bossbar condivide lo spazio con
le altre bossbar e puo' essere nascosta dalle impostazioni del client.
