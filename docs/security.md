---
layout: landing-page
title: Productvisie Haal Centraal
---

# Security

## Als je met API’s gaat werken, heb je andere security voorzieningen nodig dan nu. Deze set voorzieningen is een belangrijke voorwaarde voor de transitie naar API’s. In dit hoofdstuk lees je hoe je de security kunt inrichten om veilig te werken met Haal Centraal API’s. 

## Veilig gebruik van vertrouwelijke gegevens
De kern van veilig gebruik van een Haal Centraal API met vertrouwelijke gegevens is:
* Dat uitsluitend geautoriseerde (gebruikers van) applicaties toegang krijgen tot gegevens.
* Dat gebruikers uitsluitend toegang krijgen tot gegevens waarvoor zij zijn geautoriseerd.
* Dat een (SaaS)applicatie uitsluitend toegang krijgt tot de gegevens namens een gebruiker van jouw gemeente, dus alleen als jouw medewerker achter de knoppen zit.
 
## Security inrichten op veilig gebruik
Om veilig te kunnen werken met API’s heb je de volgende onderdelen nodig.
* (Toegangs)beveiliging, autorisatie en filtering
* IAM-systeem: beheren van identiteit, rollen en rechten
* Logging- en protocollering: controle achteraf en misbruik voorkomen

Hieronder lees je een uitwerking van deze onderdelen

### (Toegangs)beveiliging, autorisatie en filtering
Gemeenten bieden een breed palet aan producten en diensten die allemaal een andere minimale set gegevens en functionaliteit nodig hebben. En die producten en diensten worden geleverd door veel verschillende medewerkers met verschillende rollen en rechten. 

Gemeenten moeten hiervoor zelf de toegangsbeveiliging en autorisatie organiseren. Gemeenten hebben daarvoor minimaal nodig:

* Identity Provider (IP): authenticeren van de eindgebruiker.
* Security Token Service (STS): beheren van security tokens en identificeren van een client (SaaS) applicatie.
* API Gateway: (toegangs)beveiliging van de API’s.
* Proxy of een ‘facade’: autorisatie op detailniveau.

In het kader [Uitwerking (Toegangs)beveiliging, autorisatie en filtering](https://github.com/VNG-Realisatie/Haal-Centraal-new/blob/main/docs/security.md#uitwerking-toegangsbeveiliging-autorisatie-en-filtering)lees je een uitwerking van deze onderdelen.

### IGA-systeem: beheren van identiteit, rollen en rechten
Bij voorkeur wordt de Identity Provider gevoed door een IGA (voorheen IAM) systeem, waarmee je de rollen en rechten van jouw gebruikers voor verschillende systemen centraal kunt beheren. 

Een zogenaamde ‘identity governance and administration’ (IGA) oplossing: 
* automatiseert bijvoorbeeld het creëren, updaten en verwijderen van accounts; 
* behandelt aanvragen van gebruikers om toegang te krijgen tot een bepaald systeem; 
* beheert wachtwoorden, gebruikerstoegang en toegangscertificeringsprocessen. 

Je kunt het IAM systeem koppelen aan het HR systeem, zodat een medewerker bijvoorbeeld automatisch alle rechten verliest op het gebruik van BRP gegevens als hij/zij voor een andere afdeling gaat werken.

Zo’n IGA voorziening is optioneel maar heel belangrijk, zeker als je in een wat grotere gemeente werkt. Het beheren van veel gebruikers met verschillende accounts in allerlei processystemen zoals nu in veel gemeenten gebruikelijk is, is een beveiligingsrisico.

### Logging- en protocollering: controle achteraf en voorkomen misbruik
Een gemeente moet conform de wet BRP alle BRP bevragingen protocolleren. Dat gebeurt nu meestal in de diverse procesapplicaties. Het is beter om een centrale logging- of protocolleringsvoorziening in te richten, waarin API requests en evt. ook responses onweerlegbaar worden vastgelegd, samen met het token dat de identiteit en claims van de eindgebruiker bevat. 

Door de API Gateway te laten loggen en de toegangsbeveiliging voor nieuwe applicaties te baseren op eindgebruikercredentials hoef je straks in de meeste gevallen niet meer te protocolleren in de afnemende applicatie. Ook kun je burgerverzoeken in het kader van de AVG beter en sneller afhandelen door de logginggegevens te verrijken met de informatie uit je verwerkingsregister. 

Voor het verzamelen, opslaan en analyse van de logging kun je bijvoorbeeld gebruik maken van de ELK (Elastic search, Logstash en Kibana), Stack, Splunk, LogRhythm, Graylog, etc.

------------------

## Uitwerking (Toegangs)beveiliging, autorisatie en filtering

### Identity Provider (IP)	
Voor het authenticeren van de eindgebruiker waarin de claims voor het gebruik van de API van alle gebruikers van jouw gemeente centraal zijn vastgelegd. 

Nadat de Identity provider heeft vastgesteld wie de ingelogde gebruiker is en welke applicatie de API namens de gebruiker wil bevragen, kunnen tokens (al dan niet met gebruikersclaims) aan client applicaties worden verstrekt. 

Hiermee kan de client (SaaS)applicatie namens de gebruiker de API bevragen.

### Security Token Service (STS)	
Voor het uitgeven, valideren, vernieuwen en beëindigen van security tokens en het veilig identificeren van een client (SaaS) applicatie. Hoort bij de Identity Provider.

### API Gateway	
Voor de (toegangs)beveiliging van de API’s. Een API Gateway is vaak onderdeel van een product voor ‘full life cycle API Management’. 

Een API Gateway bevat ondersteuning voor het design, publiceren, documenteren, beveiligen en analyseren van API’s. Zie de website van Gartner voor productinspiratie. 

Een API Gateway is een must have voor iedere gemeente die gevoelige API’s aan afnemers aanbiedt.
