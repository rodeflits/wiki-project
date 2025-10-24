# FiveM Servers
Een **FiveM server** kan worden opgezet op een **localhost**, **game dedicated server** of **VPS**.  
[Officiële documentatie](https://docs.fivem.net/docs/server-manual/setting-up-a-server/)
---
## Frameworks

Na het opzetten van je server kun je ervoor kiezen om een **Framework** te gebruiken.  
Een framework biedt een **architectuurlaag** voor je serverstructuur, gameplay en spelersinteractie bovenop de **FiveM API**.

### Wat doet een Framework?
Een framework bouwt een extra laag met:
1. Structuur voor spelers (jobs, inventory, money, etc.)
2. Databasekoppeling (meestal **MySQL** of **MariaDB**)
3. Server ↔ Client synchronisatie

Daarnaast bevatten frameworks al **basis-scripts** die onder andere:
- De logica regelen voor economie, jobs en permissions  
- Communiceren met de database  
- UI, animaties en voertuighandelingen afhandelen  
---

## Bekende Frameworks
| Framework | Beschrijving |
|------------|---------------|
| **ESX** | Oud, de grootste community en veel support |
| **QBCore** | Modern, cleane codebase |
| **OX_Core** | Nieuwste generatie, wordt gebruikt in high-end servers |

---
## Eigen scripts

Hoewel een framework een sterke basislaag biedt, moet je vaak nog **eigen scripts schrijven of toevoegen** om een unieke server te krijgen.  

Meer info: [Scripts](scripts.md)