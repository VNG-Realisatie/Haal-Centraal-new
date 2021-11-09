---
layout: landing-page
title: Startgids
---
# Startgids

## Met Haal Centraal API’s kun je als gemeente gegevens rechtstreeks bij de landelijke registratie bevragen. Dat is beter, sneller en goedkoper. In deze startgids lees je hoe je als gemeente start met Haal Centraal API’s.
{:.header}
&nbsp;   
## Start op 2 sporen tegelijk met Haal Centraal API’s  
{:.header}
We adviseren om op 2 sporen tegelijk te starten met Haal Centraal API’s.
   
* Spoor 1: start direct met Haal Centraal door de eerste afnemer op een Haal Centraal API aan te sluiten. Zo doe je belangrijke ervaring op met de API’s. En vanaf de eerste API heb je al voordeel in kosten, snelheid en gemak. 
      
* Spoor 2: start tegelijk met de transitie naar het volledig werken met API’s bij je gemeente. Deze transitie vraagt tijd en voorbereiding. Als je de transitie volledig hebt afgerond, kun je het administratieve gegevensmagazijn en veel lokale kopieën uitfaseren. Als je selecties en data-analyses uitvoert op het gegevensmagazijn kun je een hiervoor geoptimaliseerd systeem aanschaffen.

&nbsp;   
## Spoor 1: direct starten met de eerste API
{:.header}
Start direct met Haal Centraal door de eerste API aan te sluiten.  
   
### Voorwaarden spoor 1
{:.header}
   
* De BAG (Basisregistratie Adressen en Gebouwen) is een openbare bron. Je kunt hier zonder API gateway op aansluiten. Maar het handiger om wel een API gateway te gebruiken, omdat de andere HC API’s hier naar verwijzen.  
* In de BRP (Basisregistratie Personen), BRK (Basisregistratie Kadaster) en WOZ API staan vertrouwelijke gegevens. Hiervoor heb je een API gateway nodig. 
[Lees meer over API gateways](https://vng-realisatie.github.io/Haal-Centraal-new/security#api-gateway).
   
### Stappenplan spoor 1
{:.header}
1.	Verwijs je leverancier naar de [Getting started guide van de API op GitHub](https://vng-realisatie.github.io/Haal-Centraal-new/aansluiten-op-apis). Daar vindt hij alle informatie om de API aan te sluiten.
2.	Publiceer de API op de API Gateway van de gemeente. Regel hierin de rechten van de afnemersapplicatie als de API vertrouwelijk is, en vraag de applicatie evt. om de bevragingen te protocolleren.
3.	Voer een audit uit op de aansluiting (alleen bij vertrouwelijke API’s).

&nbsp;   
## Spoor 2: transitie – uitfaseren administratief gegevensmagazijn en kopieën
{:.header}
Start tegelijk met de transitie naar het volledig werken met API’s bij je gemeente.
   
### Voorwaarden spoor 2
{:.header}
Als je meer API’s gaat aansluiten, ga je ook de security opschalen. Hierover gaat stap 2 van het onderstaande 'Stappenplan spoor 2'.
   
### Stappenplan spoor 2
{:.header}
   
1.	Maak een transitieplan. Dat begint met een analyse van je applicatielandschap: waar sta je nu en waar wil je heen? Vervolgens kun je [migratiestrategieën toepassen](./transitieplan.md#stap-1----maak-een-transitieplan).
2.	Gefaseerd security opschalen. Als je meer API’s gaat aansluiten, ga je ook je [security gefaseerd opschalen](./transitieplan.md#stap-2--gefaseerd-security-opschalen). Concreet beweeg je van “alle security in de applicatie” naar “security in door de gemeente gecontroleerde centrale voorzieningen”. 
    
Je leest een uitgebreid stappenplan voor deze transitie in [het onderdeel Transitieplan](https://vng-realisatie.github.io/Haal-Centraal-new/transitieplan).

&nbsp;
## We staan klaar om je te helpen 
{:.header}
Heb je vragen? Neem contact met ons op.
    
* Vragen over transitie: [Cathy Dingemanse](mailto:cathy.dingemanse@denhaag.nl)
* Vragen over security: [Melvin Lee](mailto:melvin.lee@iswish.nl)
* Vragen over API's: [Robert Melskens](mailto:robert.melskens@vng.nl) en [Johan Boer](mailto:johan.boer@vng.nl)
