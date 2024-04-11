# Installasjonsguide for LK IC.2 med Home Assistant

Denne veiledningen beskriver hvordan du integrerer LK IC.2 med Home Assistant ved bruk av en Raspberry Pi og Elfin EW11-modulen. Følg disse trinnene for å sette opp ditt smarte hjem-grensesnitt.
Du trenger også en strømadapter for Elfin hvor jeg brukte https://www.clasohlson.com/no/Nettadapter-12-V-AC-36-W/p/Pr513228000 

## Forutsetninger
- **Raspberry Pi**: Versjon 3 eller 4.
- **Home Assistant**: Installert og kjørende på din Raspberry Pi.
- **Elfin EW11**: Modul koblet til IC.2s bussport.

## Installasjonstrinn

### Trinn 1: Koble til Elfin EW11
1. Koble Elfin EW11 til bussporten på IC.2.
2. Slå på enheten for automatisk å opprette et tilgangspunkt (AP).

### Trinn 2: Konfigurer nettverksinnstillinger
- Koble Elfin EW11 til det samme Wi-Fi-nettverket som din Home Assistant.

### Trinn 3: Innstillinger for serieport
Konfigurer serieporten med følgende innstillinger:
- **Baudrate**: 38400
- **Databit**: 8
- **Stoppbit**: 1
- **Paritet**: Ingen

### Trinn 4: CLI-innstillinger
Still inn CLI for å kommunisere med følgende spesifikasjoner:
- **CLI**: Seriell Streng
- **Seriell Streng**: `+++`
- **Ventetid**: 300 ms

### Trinn 5: Sett kommunikasjonsprotokoll
- **Protokoll**: Modbus

### Trinn 6: oppdatere configuration.yaml i Home Assistant

## Tilleggsressurser
For mer informasjon om Elfin EW11, se [produktsiden på AliExpress](https://www.aliexpress.com/item/4000533274909.html).

