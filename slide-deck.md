---
marp: true
---

TALK Extension

---

Sommaire


---

|||
|---|---|
|Théo Bougé|https://theobouge.eu|
|Benoît Masson||


---

## 1. Histoire + Tech

---

### 1a. Histoire (Benoît)

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
     - **quizz**
         - fr
         - com
         - co
         - gouv.fr
         - bzh
         - paris
         - eu
         - asia
         - ευ
         - yt
         - dev
         - ai
         - tv
         - radio
     => règle 2 caractères
- IDN
(- extension .arpa)

---

### 1b. DNS (Théo)

![URI](assets/dns.svg)

---

# Record DNS

- TXT
- A / AAAA
- NS
- MX
- CNAME / DNAME
- DNSKEY


---

# Quizz

- comment trouver toto.fr ? 
- comment trouver toto.gouv.fr ?
- comment trouver toto.co.uk ?
- comment trouver toto.fr.com ? 

---


# Les DNS racines alternatifs

## https://opennic.org/

```
~ 
❯ dig +short be.libre

~ 
❯ dig @94.247.43.254 +short be.libre
161.97.219.84

```

## .onion

https://www.torproject.org/fr/download/

---

### 1c. Whois/RDAP (Théo)

https://client.rdap.org/?type=domain&object=adatechschool.fr

---

## 2. Acteurs (Benoît)

- Icann, gouvernements
- registry, backend
- registrar (OVHcloud)
- registrant

- proxy (RRPproxy)

- domainer
- spammers, phishers

---

## 3. ccTLDs (Théo)

**quizz** pays correspondant ?

- tv, ai, yt
- ly, io
- af
- hr

---

## 4. gTLDs 2012

(Benoît)

- intro (7 en 1985 : com, net, org, edu, gov, mil, int + 7 en 2000 :
aero, biz, coop, info, museum, name, pro + 6 en 2004 : asia, cat, jobs,
mobi, tel, travel)
     => ouverture massive en 2012 (objectifs, process, coût 180k$, …)
     => dernières validations en 2022
(https://newgtlds.icann.org/en/program-status/delegated-strings)
     - .yun (validé 2016, arrive bientôt)

- B .ευ (langues chine/arabe/hébreu)
- T .leclerc / .cuisinella (entreprises, usage interne)

---

- B .ovh (entreprise, en vente publique)
- T .sncf / .goodyear (plus utilisés / supprimés)

---

- B .app (HTTPS only)
- T .security, .auto (cher)

---

- B .sucks (racket)
- T .example / .local (non routés) + .corp / .home (dossiers refusés)
- B .amazon / .web (conflits)

---

- Bilan
     => chiffres (stats, top 5 coût réel)

---

## 5. New round 2026 (Benoît)

- roadmap
- prix
(http://gw2sdev-docker:21119/b/MYNpkPzyRaEcHo5KE/prez-extension/ZzcXw5kX67FFzpuav)
- perspectives ?
     - de vente pour les demandeurs de dossier => vente forcée auprès
des grosses marques
     - grand public => pas d'extension révolutionnaire a priori, ça va
pas changer grand chose

---

## 6. Ouvertures (Théo)

- Aftermarket
- NFT, Web 3
     - .agi ? https://domainincite.com/31315-ai-rival-lines-up-gtld-bid
/
https://unstoppabledomains.com/blog/categories/announcements/article/agi-tld