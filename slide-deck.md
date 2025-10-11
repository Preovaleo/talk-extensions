---
marp: true
headingDivider: []
theme: uncover
class:
  - invert
---

<!-- markdownlint-disable MD001 MD026 MD033 MD045 -->

<!-- Compile to HTML with `marp -w -s --html true .`
     (if it raises a watch error, disable git FS monitoring first with `git config core.fsmonitor false`) -->

<!-- https://marpit.marp.app/markdown -->

<style>
    @import url('./slide-deck.css');
</style>

<div class="flex vertical center">

![bg cover opacity:0.7](./assets/network.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@choys_">Conny Schneider</a> sur <a href="https://unsplash.com/fr/photos/a-blue-background-with-lines-and-dots-xuTJZ7uD7PI">Unsplash</a> -->

# La grande histoire

## des petites **extensions**

### de **noms de domaines**

<div class="spacer"/>

Théo Bougé & Benoît Masson – OVHcloud

</div>

---

<div class="flex vertical space-between">

## Qui sommes-nous ?

<div class="horizontal space-around">

<div class="vertical start">

### Théo

![width:200px](./assets/theo.png)

SRE Domaines

</div>
<div class="vertical start">

### Benoît

![width:200px](./assets/benoit.jpg)

Développeur Domaines

</div>

</div>

![width:300px](./assets/logo%20ovhcloud.png)

</div>

---

![bg cover opacity:0.5](./assets/dictionary.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@joshua_hoehne">Joshua Hoehne</a> sur <a href="https://unsplash.com/fr/photos/papier-dimprimante-blanc-avec-texte-noir-1UDjq8s8cy0">Unsplash</a> -->

<div class="flex vertical space-around">

# 1. Noms de domaines

</div>

---

<div class="flex vertical start">

## Histoire (Benoît)

- c'est quoi un NDD
- illustrer sur une URL type
  http://gw2sdev-docker:21119/b/MYNpkPzyRaEcHo5KE/prez-extension
- **quizz**
  - toto.fr
  - com.toto.fr (fr)
  - toto.gouv.fr (gouv.fr)
  - toto.com.fr (com.fr)
  - toto.fr.com (com)
  - toto.notaires.fr (fr mais…)
- tld vs sld vs extension
  https://publicsuffix.org/list/
- ccTLDs vs gTLDs
  - **quizz** - fr - com - co - gouv.fr - bzh - paris - eu - asia - ευ - yt - dev - ai - tv - radio
    => règle 2 caractères
- IDN
  (- extension .arpa)

</div>

---

![bg cover opacity:0.5](./assets/directions.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@j_harris_391">Joshua Harris</a> sur <a href="https://unsplash.com/fr/photos/un-poteau-avec-un-tas-de-panneaux-de-signalisation-jaunes-dessus-BwH31YGYXho">Unsplash</a> -->

<div class="flex vertical space-around">

# 2. DNS

</div>

---

<div class="flex vertical start">

## DNS (Théo)

![URI height:500px](assets/dns.svg)

</div>

---

<div class="flex vertical start">

## Record DNS

- TXT
- A / AAAA
- NS
- MX
- CNAME / DNAME
- DNSKEY

</div>

---

<div class="flex vertical start">

## Quizz

- comment trouver toto.fr ?
- comment trouver toto.gouv.fr ?
- comment trouver toto.co.uk ?
- comment trouver toto.fr.com ?

</div>

---

<div class="flex vertical start">

## Les DNS racines alternatifs

### https://opennic.org/

```sh
~
❯ dig +short be.libre

~
❯ dig @94.247.43.254 +short be.libre
161.97.219.84

```

### .onion

https://www.torproject.org/fr/download/

</div>

---

![bg cover opacity:0.3](./assets/phone-book.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@portmorien">Port Morien Digital Archive</a> sur <a href="https://unsplash.com/fr/photos/xPUzCnR_Vrw">Unsplash</a> -->

<div class="flex vertical space-around">

# 3. Annuaire Whois/RDAP

</div>

---

## Whois/RDAP (Théo)

https://client.rdap.org/?type=domain&object=adatechschool.fr

</div>

---

![bg cover opacity:0.8](./assets/actors.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@kyleunderscorehead">Kyle Head</a> sur <a href="https://unsplash.com/fr/photos/silhouette-de-trois-interpretes-sur-scene-p6rNTdAPbuk">Unsplash</a> -->

<div class="flex vertical space-around">

# 4. Acteurs

</div>

---

<div class="flex vertical start">

## Acteurs (Benoît)

- Icann, gouvernements
- registry, backend
- registrar (OVHcloud)
- registrant

- proxy (RRPproxy)

- domainer
- spammers, phishers

</div>

---

![bg cover opacity:0.7](./assets/countries.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@lemonvlad">Vladislav Klapin</a> sur <a href="https://unsplash.com/fr/photos/pavillon-assorti-YeO44yVTl20">Unsplash</a> -->

<div class="flex vertical space-around">

# 5. Country-Codes TLDs (ccTLDs)

</div>

---

<div class="flex vertical start">

## ccTLDs (Théo)

**quizz** pays correspondant ?

- tv, ai, yt
- ly, io
- af
- hr

</div>

---

![bg cover opacity:0.8](./assets/earth.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@carl_wang">Carl Wang</a> sur <a href="https://unsplash.com/fr/photos/une-vue-de-la-terre-depuis-lespace-OCe8cTGymSQ">Unsplash</a> -->

<div class="flex vertical space-around">

# 6. Generic TLDs (gTLDs)

</div>

---

<div class="flex vertical start">

## gTLDs 2012

(Benoît)

- intro (7 en 1985 : com, net, org, edu, gov, mil, int + 7 en 2000 :
  aero, biz, coop, info, museum, name, pro + 6 en 2004 : asia, cat, jobs,
  mobi, tel, travel)
  => ouverture massive en 2012 (objectifs, process, coût 180k$, …)
  => dernières validations en 2022
  (https://newgtlds.icann.org/en/program-status/delegated-strings) - .yun (validé 2016, arrive bientôt)

- B .ευ (langues chine/arabe/hébreu)
- T .leclerc / .cuisinella (entreprises, usage interne)

</div>

---

<div class="flex vertical start">

- B .ovh (entreprise, en vente publique)
- T .sncf / .goodyear (plus utilisés / supprimés)

</div>

---

<div class="flex vertical start">

- B .app (HTTPS only)
- T .security, .auto (cher)

</div>

---

<div class="flex vertical start">

- B .sucks (racket)
- T .example / .local (non routés) + .corp / .home (dossiers refusés)
- B .amazon / .web (conflits)

</div>

---

<div class="flex vertical start">

- Bilan
  => chiffres (stats, top 5 coût réel)

</div>

---

![bg cover opacity:0.7](./assets/2026.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@simonesecci">Simone Secci</a> sur <a href="https://unsplash.com/fr/photos/lettres-rouges-neon-49uySSA678U">Unsplash</a> -->

<div class="flex vertical space-around">

# 7. Nouveau round gTLDs

</div>

---

<div class="flex vertical start">

## New round 2026 (Benoît)

- roadmap
- prix
  (http://gw2sdev-docker:21119/b/MYNpkPzyRaEcHo5KE/prez-extension/ZzcXw5kX67FFzpuav)
- perspectives ? - de vente pour les demandeurs de dossier => vente forcée auprès
  des grosses marques - grand public => pas d'extension révolutionnaire a priori, ça va
  pas changer grand chose

</div>

---

![bg cover opacity:0.7](./assets/ideas.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@impatrickt">Patrick Tomasso</a> sur <a href="https://unsplash.com/fr/photos/ampoules-vintage-allumees-1NTFSnV-KLs">Unsplash</a> -->

<div class="flex vertical space-around">

# 8. Autres marchés

</div>

---

<div class="flex vertical start">

## Ouvertures (Théo)

- Aftermarket
- NFT, Web 3 - .agi ? https://domainincite.com/31315-ai-rival-lines-up-gtld-bid
  /
  https://unstoppabledomains.com/blog/categories/announcements/article/agi-tld

</div>

---

![bg cover](./assets/question.jpg)

<!-- Photo de <a href="https://unsplash.com/fr/@simonesecci">Simone Secci</a> sur <a href="https://unsplash.com/fr/photos/lettres-rouges-neon-49uySSA678U">Unsplash</a> -->

<div class="flex vertical space-between">

# Questions

<div class="footnotes">

Images credits: [Unsplash](https://unsplash.com)
Slides: [https://github.com/Preovaleo/talk-extensions](https://https://github.com/Preovaleo/talk-extensions/)

</div>
