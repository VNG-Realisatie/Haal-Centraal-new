---
layout: default
title: Productvisie Haal Centraal
---
# Productvisie Haal Centraal 

## Doel
Doel van het programma Haal Centraal is om de verstrekking van basisgegevens aan binnengemeentelijke afnemers te outsourcen naar Landelijke Registraties (RvIG, Kadaster, KVK). Dit moet leiden tot een forse reductie van lokale kopieën bij gemeenten. 

Haal Centraal wil voor iedere activiteit op een lokale kopie een alternatief te bieden in de vorm van een API van een landelijke registratie. We beginnen met REST API's voor het zoeken en raadplegen van basisgegevens. Speciaal voor WOZ en Erfpacht staan ook Publish Subscribe API's op onze roadmap voor het bevragen van domain events uit een Event Store, en onderzoeken we het in samenhang bevragen van basisregistraties voor analyses voor handhaving en fraudebestrijding.     


### Toegevoegde waarde voor gemeenten
- sneller & goedkoper aansluiten door best mogelijke DX
- goedkoper beheer door design voor evolvability en extensibility
- lagere investeringen (geen lokale kopie/ gegevensmagazijn)
- lagere beheerkosten (geen beheer lokale kopieën)
- hogere ROI: hergebruik API Landelijke Registratie door alle gemeentelijke taakapplicaties
- betere technologie-business alignment (Landelijke Registratie voert sneller een wijziging door dan 355 afzonderlijke gemeenten)
- biedt ruimte voor focus op de businessvraag van afnemers (i.p.v. op betrouwbaarheid en actualiteit van lokale kopieën)
- maximale compliancy op de gemeentelijke softwaremarkt (aansluiting gemeente x = 100% herbruikbaar in gemeente y)

### Toegevoegde waarde voor leveranciers
- leveranciers kunnen zich conform de wens van gemeenten richten op het bieden van toegevoegde waarde voor burgers, bedrijven en medewerkers en hun core domain i.p.v. plumbing concerns in supporting domains zoals het gebruik van basisgegevens. 

## Context
Haal Centraal is een G5 initiatief (Amsterdam, Rotterdam, Den Haag, Utrecht en Eindhoven). Het concept is getoetst in de BRK pilot van de gemeente Den Haag met het Kadaster op basis van de RSGB bevragingen standaard (voorloper BRP- en BRK-bevragen). De businesscase is gebaseerd op ervaringscijfers van de gemeente Den Haag en de softwareontwikkeling gedurende de pilot. 

## Productvisie

### Business driven 
Resourcedefinitie en functionaliteit op basis van de businessvraag van de grootste gemene infobehoefte van alle binnengemeentelijke afnemers van NL. 
Niet te verwarren met modelgedreven ontwikkeling (MDD), waarbij de definitie is gebaseerd op het providerperspectief. Haal Centraal API's zijn meestal wel herleidbaar naar een onliggend informatiemodel (zodat de realiseerbaarheid en semantiek van de API geborgd is) maar zijn zoveel mogelijk loosely coupled. Implementation bleed en tight coupling met provider implementatiedetails wordt voorkomen.

### Consumer first
Beleg de voordelen waar mogelijk bij de consumer (=binnengemeentelijke afnemer) vanwege de hefboomwerking: complexiteit bij de provider (1x bouwen en beheren), de voordelen in kosten en doorlooptijd bij de consumer ((aantal binnengemeentelijke afnemers x 351) x bouwen en beheren)

### Developer first
Focus op bruikbaarheid voor de ontwikkelaar: OAS spec is getest op codegeneratie (Java, .NET en Python, het meest gebruikt in gemeentelijke markt), ontwerpbeslissingen zijn getoetst op het effect op de code, maximale consistentie met andere Haal Centraal API’s en behaviour driven development (BDD) scenario's in Gherkin om het gedrag van de API te beschrijven.

### Contract first
…en niet code first. De API is agnostisch, vrij van implementatiedetails van het providersysteem en niet gevoelig voor wijzigingen in systeemlogica bij de provider.

### Agnostisch
= zonder kennis van de consumer. De API moet door alle (in theorie 200 verschillende) gemeentelijke processen en producten van andere overheidspartijen kunnen worden gebruikt die basisgegevens nodig hebben.

### Evolvable
Haal Centraal API's zijn uitbreidbaar en evolvable. Doel is om geen of zo min mogelijk breaking changes te introduceren.

### Geïmplementeerd 
API's worden geimplementeerd door een landelijke registratie (RvIG, kadaster, KVK, etc.)

### Non functionals:
- supersnel
- schaalbaar
- betrouwbaar
- resilient
- vastgelegd in een SLA en een Dossier Afspraken en Procedures

## Scope
Ontwerp o.b.v. een inventarisatie informatiebehoefte van binnengemeentelijke afnemers. De scope is beperkt tot de basisgegevens waarover de landelijke registratie beschikt. 

## Uitgangspunten
- Alle code, documenten en specificaties die ontstaan in dit traject wordt Open Source gepubliceerd onder de
[EUPL licentie](https://joinup.ec.europa.eu/collection/eupl/eupl-text-11-12);
- Voor de specificatie van API's wordt [OpenAPI Specification v3.x](https://www.forumstandaardisatie.nl/standaard/openapi-specification) 
gebruikt. Deze is door Forum Standaardisatie op de
["Pas toe of leg uit"-lijst](https://www.forumstandaardisatie.nl/lijst-open-standaarden/in_lijst/verplicht-pas-toe-leg-uit)
geplaatst;
- Waar mogelijk worden de
[API strategie](https://docs.geostandaarden.nl/api/API-Strategie/) en de [REST API Design Rules](https://docs.geostandaarden.nl/api/API-Designrules/) 
toegepast.

## Realisatie
We werken zoveel mogelijk Agile. Onderstaande activiteiten zijn onderdeel van een iteratief proces.
- we maken van iedere gemeentelijke informatiebehoefte een user story. 
- user stories worden gemapt op een een Goals Canvas, waarmee we de basisfuncties en endpoints van API specificeren. 
- Voor de meest voorkomende stories maken we een definitie in OpenAPI (en als het nodig is features voor de provider). 
- een designer van VNG Realisatie definieert de API in OpenAPI i.s.m. de PO, een domeinexpert en ontwikkelaar van de landelijke registratie, een tester, en een developer van VNG Realisatie. 
- iedere definitie is getoetst op DX, waaronder code-generatie door een developer van VNG Realisatie, onze eigen customer zero. 
- de (concept)definitie wordt gerealiseerd door een landelijke partij
- de definitie wordt bijgesteld op basis van vragen en opmerkingen van provider en andere stakeholders, bijvoorbeeld n.a.v. een fieldlab
- testen worden primair uitgevoerd door de landelijke registratie, maar ook door minimaal 1 gemeente. 
- (een versie van) de API wordt in productie genomen en beheerd door Landelijke Registratie
- onboarding via de Landelijke registratie, documentatie via Haal Centraal repository op Github.

