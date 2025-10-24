# FiveM Scripts

Scripts vormen het **een FiveM-server**. Ze bepalen de gameplay
Met scripts bouw je jouw unieke serverervaring bovenop het gekozen **Framework**.

---

## Hoe werken scripts?

FiveM maakt gebruik van een **Client-Server architectuur**:
- **Client-side scripts** draaien op de computer van de speler.  
- **Server-side scripts** draaien op de game server.  
Beide communiceren via **events**.

### 🔸 Server-side
Behandelt de “harde logica”:
- Database transacties (geld, items, voertuigen)
- Jobs, economie, permissions
- Triggers naar clients sturen (bijv. UI-update, notitie tonen)

> Bestandstypen:  
> `server.lua`, `server.js`, `server.cs`

### 🔹 Client-side
Behandelt de “visuele en interactieve logica”:
- UI (menus, notificaties)
- Animaties, camera’s, voertuighandelingen
- Gebruikersinput (toetsen, muis)

> Bestandstypen:  
> `client.lua`, `client.js`, `client.cs`

---

## Event-communicatie

De client en server praten d.m.v. **events**.  
Voorbeeld in **Lua** (meest gebruikte taal voor FiveM):

```lua
-- Client-side
RegisterCommand("betaal", function()
    TriggerServerEvent("bank:betaalSpeler", 500)
end)

-- Server-side
RegisterNetEvent("bank:betaalSpeler")
AddEventHandler("bank:betaalSpeler", function(amount)
    print("Speler betaalde: $" .. amount)
end)