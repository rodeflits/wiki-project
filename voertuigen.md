# Voertuigen in FiveM

Voertuigen zijn een belangrijk onderdeel van vrijwel elke FiveM server. Ze bepalen niet alleen het transport, maar ook de ervaring van de speler.

---

## Overzicht

Een voertuigresource bevat de volgende bestanden:
- `.yft` – modelbestand (3D model en onderdelen)
- `.ytd` – texturen (kleuren, interieur, lichten)
- `.meta` – configuratie (handlingen, geluiden, data)

Voorbeelden van meta-bestanden:
- `vehicles.meta` – algemene voertuigdata (modelnaam, handling-id, class)
- `carvariations.meta` – kleur- en livery-opties
- `carcols.meta` – lichtkleuren en kleurvariaties
- `handling.meta` – rijgedrag, snelheid, remmen, gewicht, etc.

---

## Voertuigen toevoegen

Voertuigen worden als aparte **resources** toegevoegd in de `resources` map.  
Elke voertuigresource bevat een `fxmanifest.lua` die beschrijft welke bestanden moeten worden geladen.

Voorbeeld:
```lua
fx_version 'cerulean'
game 'gta5'

files {
    'data/vehicles.meta',
    'data/carvariations.meta',
    'data/carcols.meta',
    'data/handling.meta'
}

data_file 'VEHICLE_METADATA_FILE' 'data/vehicles.meta'
data_file 'CARCOLS_FILE' 'data/carcols.meta'
data_file 'VEHICLE_VARIATION_FILE' 'data/carvariations.meta'
data_file 'HANDLING_FILE' 'data/handling.meta'