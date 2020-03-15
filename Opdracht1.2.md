# Browser Technologies

## Opdracht 1.2 - Fork je OBA

Deze opdracht heb ik vanwege ziekte gemist. Omdat ik geen drie verschillende devices tot mijn beschikking heb (alleen mijn MacBook en iPhone, maar op beide werkt de app en is er niet veel verschil), kan ik daar niet op testen.

Ik heb getest op mijn [web applicatie van WAFS](https://github.com/martendebruijn/web-app-from-scratch-1920).

- [Features](#Features)
- [Browsers](#Browsers)
- [Screenreader](#Screenreader)

## Features

## 1. Afbeeldingen uitzetten

Als ik via de [Web Developer Extentie](https://chrome.google.com/webstore/detail/web-developer/bfbameneiokkgbdmiekhjnmfkcnldhhm) de afbeeldingen uitzet, worden de afbeeldingen niet meer weergeven, maar i.p.v. de alt tekst. De app zelf werkt.

##### Overview pagina zonder afbeeldingen

![Overview page without img](/img/overview-without-img.png)

##### Detail pagina zonder afbeeldingen

![Detail page without img](/img/detail-without-img.png)

### Oplossing

Ik zou ervoor kunnen kiezen om een placeholder afbeelding toe te voegen.

## 2. Custom Fonts uitzetten

Wanneer ik via de [Font blocker Extentie](https://chrome.google.com/webstore/detail/font-blocker/knpgaobajhnhgkhhoopjepghknapnikl) customs fonts uitzet, gebeurt er niets.

### Oplossing

Een oplossing voor wanneer custom fonts niet laden / zijn uitgezet, zijn het gebruik van fall-back fonts. En controleren dat dan alles nog leesbaar is, zichtbaar en functioneel.

## 3. Kleur en kleurenblindheid

### Kleur

Leesbaarheid is belangrijk, de leesbaarheid hangt onderandere erg af van het contrast tussen de kleur van de achtergrond en die van de voorgrond. Dit kan men testen m.b.v. websites als:
[Hele pagina - Check My Colours](https://www.checkmycolours.com/)
[Kleuren tester (handige tool voor bij het ontwerpen) - Colorable](https://colorable.jxnblk.com/)

Wanneer ik mijn web applicatie in de checkmycolours zet, komt eruit dat al mijn elementen een goed contrast heeft.

### Oplossing

Een oplossing voor wanneer dit niet het geval zou zijn, is het ervoor zorgen dat de voorgrondkleur en achtergrondkleur beter op elkaar zijn afgestemd en een betere contrast ratio heeft.

### Kleurenblindheid

Met de [Colorblinding Extentie](https://chrome.google.com/webstore/detail/colorblinding/dgbgleaofjainknadoffbjkclicbbgaa/related) kan men testen hoe zijn website eruit ziet als men kleurenblind is. Met deze extentie heb je verschillende vormen van kleurenblind zijn. Iedere kleurenblindheid modus had effect op mijn web applicatie. Hoewel degehele website goed leesbaar blijft in iedere modus, worden de kleuren van het beginscherm anders.

##### ColorBlinding menu

![Colorblinding menu](/img/colorblinding.png)

##### Normal view

![Normal](/img/normal.png)

##### Red Blind

![Red Blind](/img/red-blind.png)

##### Green Blind

![Green Blind](/img/green-blind.png)

##### Blue Blind

![Blue Blind](/img/blue-blind.png)

##### Red Weak

![Red Weak](/img/red-weak.png)

##### Green Weak

![Green weak](/img/green-weak.png)

##### Blue Weak

![Blue weak](/img/blue-weak.png)

##### Monochromacy

![Monochromacy](/img/mono.png)

##### Blue Cone Monochromacy

![Blue Cone Monochromacy](/img/blue-cone-mono.png)

##### Detail page with colorblindness

![Detail page with colorblindness](/img/detail-c-blind.png)

### Oplossing

Nu heb ik natuurlijk een applicatie gemaakt wat staat en valt met kleur
Hoewel de applicatie staat en valt met kleur, zou ik de applicatie toegankelijker kunnen maken d.m.v. het gebruik van woorden en kleur waardes. Zodat de gebruiker altijd weet welke kleur wat is.
FE: bij het keuzemenu 'Rood:' en kleurwaardes gebruiken. En bij de overviewpagina iets in de trant van 'U heeft gezocht op ....'.

## 4. Muis en trackpad werkt niet

Het keuzemenu werkt wél zonder muis, maar de gebruiker ziet niet dat een van de sliders geselecteerd zijn, waardoor het lastig is voor de gebruiker om te weten dat hij of zij de slider heeft geselecteerd. De overview- en detailpagina zijn prima te gebruiken met alleen het keyboard.

### Oplossing

Wanneer niet het geval is dat je web app / website goed werkt zonder muis of trackpad, kan men gebruik maken van keyframes. 'keypress'

## 5. Breedband internet uitzetten

Als men op een traag netwerk zit, wordt wanneer de app aan het laden is een loader getoont. Daarna laad hij de overzichtpagina, zonder afbeeldingen, prima. Om de afbeeldingen te laden heeft hij erg veel tijd voor nodig.

### Oplossing

Dit zou ik op kunnen lossen door gebruik te maken van afbeeldingen van een mindere grootte. Ook zou ik gebruik kunnen maken van zogenoemde lazyloading. Bij lazyloading wordt eerst de content geladen en daarna pas de afbeeldingen.

## 6. Javascript (volledig)

Mijn gehele website (behalve de h1 aan de bovenkant van de pagina) wordt via JavaScript gerenderd. Hierdoor laat het dus niets zien wanneer men niet de beschikking heeft tot JavaScript.

##### De webapp zonder JavaScript

![Without JavaScript](/img/without-js.png)

### Oplossing

Om te beginnen zou ik het keuzemenu aan het begin meteen in de html zetten, zodat deze ook zonder html geladen wordt. De applicatie is een client side render applicatie. Men kan de applicatie ook omzetten naar een server-side applicatie.

## 7. LocalStorage en Cookies uitschakelen

### Oplossing

## Browsers

Iedere browser werkt anders. Een goed voorbeeld hiervan is met het werkbaar maken van nieuwe CSS features. Deze zijn soms niet te gebruiken in bepaalde browsers en soms via prefixes. Op de website [Can I use?](caniuse.com) kan men controleren of een CSS propertie werkt in verschillende browsers. Men kan gebruik maken van de query support om een bepaalde CSS propertie alleen te gebruiken wanneer de browser deze ook daadwerkelijk ondersteund.

## Chrome

Tijdens het bouwen van de webapplicatie heb ik Chrome gebruikt. In Chrome werkt alles goed.

## Firefox

In Firefox werkt alles hetzelfde.

##### Keuzemenu Firefox

![Keuzemenu Firefox](/img/firefox-1)

##### Overview pagina Firefox

![Overview pagina Firefox](/img/firefox-2)

## Safari

Ook in Safari werkt de web applicatie op dezelfde manier.

##### Keuzemenu Safari

![Keuzemenu Safari](/img/safari-1)

##### Overview pagina Safari

![Overview pagina Safari](/img/safari-2)

## Screenreader

Om de screenreader te testen heb ik de standaard screenreader van Apple gebruikt. Dit werkte verassend goed. Alles werd voorgelezen. Het enige lastige was dat als men op de overview pagina op de titel van een kunstobject drukt de gebruiker meteen door wordt gestuurd naar de detail pagina, waardoor de overview pagina minder goed te navigeren is. Deze titels worden echter wel voorgelezen wanneer men tab gebruikt i.p.v. erop te klikken.

### Oplossing

Men kan ervoor zorgen dat alles netjes wordt voorgelezen door de screenreader door gebruik te maken van semantische HTML structuur.

<!-- ### Criteria

- Zet je code op Github
- Schrijf een Readme met:
  - een beschrijving van alle features die je hebt getest
  - een beschrijving van de Devices en browsers waar je op hebt getest
  - een beschrijving van de screenreader test
  - beschrijf hoe je de problemen hebt opgelost, of hoe je dit zou oplossen (met todo’s) als je genoeg tijd en budget zou hebben -->
