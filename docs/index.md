---
layout: landing-page
title: Productvisie Haal Centraal
---
{:.landingpage-header}
# Productvisie Haal Centraal

{:.landingpage-header}
Doel van het programma Haal Centraal is om de verstrekking van basisgegevens aan gemeentelijke taakapplicaties te outsourcen naar Landelijke Registraties (RvIG, Kadaster, KVK). Dit moet leiden tot een forse reductie van lokale kopieën bij gemeenten.    
Haal Centraal biedt voor iedere activiteit op een lokale kopie een alternatief in de vorm van een API van een landelijke registratie. Te beginnen met REST API’s voor het zoeken en raadplegen van basisgegevens. Speciaal voor WOZ en Erfpacht staan ook Publish Subscribe API’s op de roadmap voor het bevragen van domain events uit een Event Store, en onderzoeken we het in samenhang bevragen van basisregistraties voor analyses voor handhaving en fraudebestrijding.
<br><br>

{:.header}
## Winst voor gemeenten

- sneller & goedkoper aansluiten door best mogelijke DX
- goedkoper beheer door design voor evolvability en extensibility
- lagere investeringen (geen lokale kopie/ gegevensmagazijn)
- lagere beheerkosten (geen beheer lokale kopieën)
- hogere ROI: hergebruik API van Landelijke Registratie door alle gemeentelijke taakapplicaties
- betere technologie-business alignment (Landelijke Registratie voert sneller een wijziging door dan 355 afzonderlijke gemeenten)
- biedt ruimte voor focus op de businessvraag van afnemers (i.p.v. op betrouwbaarheid en actualiteit van lokale kopieën)
- maximale compliancy op de gemeentelijke softwaremarkt (aansluiting gemeente x = 100% herbruikbaar in gemeente y)

{:.header}
## Winst voor leveranciers

Leveranciers kunnen zich richten op het bieden van toegevoegde waarde voor burgers, bedrijven en medewerkers en hun core domain i.p.v. “plumbing concerns” in supporting domains zoals het gebruik van basisgegevens.

{:.header}
## Context

Haal Centraal is een G5 initiatief (Amsterdam, Rotterdam, Den Haag, Utrecht en Eindhoven). De businesscase is gebaseerd op ervaringscijfers uit de pilot van de gemeente Den Haag en het Kadaster waarin het concept is beproefd.

{:.header}
## Producteigenschappen

<div class="row">
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Business driven</h3>
        <p class="card-text">
        Resourcedefinitie en functionaliteit op basis van de informatiebehoefte van alle binnengemeentelijke afnemers. Niet te verwarren met modelgedreven ontwikkeling (MDD), waarbij de definitie is gebaseerd op het providerperspectief. Haal Centraal API's zijn zoveel mogelijk loosely coupled. “Implementation bleed” en “tight coupling” met implementatiedetails van de provider wordt voorkomen.
        </p>
      </div>
    </div>
  </div>
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Consumer first</h3>
        <p class="card-text">
        In verband met de hefboomwerking wordt complexiteit zoveel mogelijk bij provider belegd in plaats van bij consumer (ontwikkeling en beheer in alle gemeentelijke taakapplicaties). Daarnaast is ontwikkeling en beheer van complexe businesslogica ook in betere handen bij een domeindeskundige provider dan bij een consumer die verstand heeft van een ander domein. Dit bespaart geld en voorkomt fouten.
        </p>
      </div>
    </div>
  </div>
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Developer first</h3>
        <p class="card-text">
        Veel aandacht voor DX:
        <ul>
            <li>Haal Centraal API specificaties zijn getest op codegeneratie (Java, .NET en Python)</li>
            <li>ontwerpbeslissingen zijn getoetst op het effect op de code</li>
            <li>maximale consistentie met andere Haal Centraal API’s</li>
            <li>BDD scenario's in Gherkin om het gedrag van de API te beschrijven</li>
        </ul>
        </p>
      </div>
    </div>
  </div>
</div>
<br>
<div class="row">
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Agnostisch</h3>
        <p class="card-text">
        = zonder kennis van de consumer. De API moet door alle (in theorie 200 verschillende) gemeentelijke processen en producten van andere overheidspartijen kunnen worden gebruikt.
        </p>
      </div>
    </div>
  </div>
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Evolvable</h3>
        <p class="card-text">
        Haal Centraal API's zijn uitbreidbaar en evolvable. Doel is om besparingen voor gemeenten te realiseren door geen of zo min mogelijk breaking changes te introduceren.
        </p>
      </div>
    </div>
  </div>
  <div class="col">
    <div class="card no-border">
      <div class="card-body">
        <h3 class="card-title">Geïmplementeerd</h3>
        <p class="card-text">
        Haal Centraal API's zijn geïmplementeerd op een landelijke registratie van RvIG, kadaster, KVK, etc.
        </p>
      </div>
    </div>
  </div>
</div>

{:.header}
## Uitgangspunten

- Alle code, documenten en specificaties die ontstaan in dit traject wordt Open Source gepubliceerd onder de [EUPL licentie](https://joinup.ec.europa.eu/collection/eupl/eupl-text-11-12)
- Voor de specificatie van API's wordt [OpenAPI Specification v3.x](https://www.forumstandaardisatie.nl/standaard/openapi-specification) of AsyncAPI Specification 2.x gebruikt.
- Waar mogelijk worden de [API Design Visie](https://github.com/Geonovum/KP-APIs/tree/master/Werkgroep%20Design%20Visie){:target="_blank"}, de [API strategie](https://docs.geostandaarden.nl/api/API-Strategie/){:target="_blank"} en de [REST API Design Rules](https://docs.geostandaarden.nl/api/API-Designrules/){:target="_blank"} toegepast.

{:.header}
## Realisatie

We werken zoveel mogelijk Agile. Onderstaande activiteiten zijn onderdeel van een iteratief proces.

- we maken van iedere gemeentelijke informatiebehoefte een user story.
- user stories worden gemapt op een Goals Canvas, waarmee we de basisfuncties en endpoints van een API specificeren.
- Voor de meest voorkomende stories maken we een definitie in OpenAPI of Async API, en als het nodig is features voor de provider. 
- iedere definitie is getoetst op DX, waaronder code-generatie door een developer van VNG Realisatie, door onze eigen customer zero.
- de (concept)definitie wordt gerealiseerd door een landelijke partij.
- de definitie wordt bijgesteld op basis van vragen en opmerkingen van provider en andere stakeholders, bijvoorbeeld n.a.v. een fieldlab.
- testen worden primair uitgevoerd door de landelijke registratie, maar ook door minimaal 1 gemeente.
- (een versie van) de API wordt in productie genomen en beheerd door Landelijke Registratie.
- onboarding via de Landelijke registratie, documentatie via Haal Centraal Github.
