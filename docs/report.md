# Praktična implementacija VLAN segmentacije u Cisco Packet Traceru

## Izrada mrežne topologije

Za implementaciju segmentacije korištena je topologija koja se sastoji od
jednog Cisco 2911 routera, jednog Cisco 2960 switcha i šest PC računala.
Router je povezan sa switchem, dok su krajnji uređaji raspoređeni po
odgovarajućim VLAN-ovima.

### VLAN raspodjela

| VLAN | Naziv       | PC uređaji | Switch portovi |
|-----:|-------------|------------|----------------|
| 10   | USERS       | PC0, PC1   | F0/2 – F0/3    |
| 20   | SERVERS     | PC2, PC3   | F0/4 – F0/5    |
| 30   | MANAGEMENT  | PC4, PC5   | F0/6 – F0/7    |

---

## Kreiranje i konfiguracija VLAN-ova

Na switchu su kreirani VLAN-ovi USERS, SERVERS i MANAGEMENT te su portovi
dodijeljeni prema pripadajućim segmentima. Time je ostvarena logička podjela
mreže bez dodatne fizičke infrastrukture.

---

## Trunk veza i router-on-a-stick konfiguracija

Između switcha i routera konfigurirana je trunk veza koja omogućuje prijenos
prometa iz više VLAN-ova preko jednog fizičkog sučelja. Na routeru je
implementirana router-on-a-stick konfiguracija s podsučeljima za svaki VLAN.

---

## Konfiguracija IP adresa

| Uređaj | IP adresa        | Subnet maska     | Gateway        |
|--------|------------------|------------------|----------------|
| PC0    | 192.168.10.10    | 255.255.255.0    | 192.168.10.1   |
| PC1    | 192.168.10.11    | 255.255.255.0    | 192.168.10.1   |
| PC2    | 192.168.20.10    | 255.255.255.0    | 192.168.20.1   |
| PC3    | 192.168.20.11    | 255.255.255.0    | 192.168.20.1   |
| PC4    | 192.168.30.10    | 255.255.255.0    | 192.168.30.1   |
| PC5    | 192.168.30.11    | 255.255.255.0    | 192.168.30.1   |

---

## Implementacija ACL pravila i testiranje

ACL pravilima ograničen je promet iz Users VLAN-a tako da je dopušten samo
HTTP promet prema Servers VLAN-u, dok je sav ostali promet blokiran.
Rezultati testiranja potvrđuju da ACL pravilno blokira neovlašteni promet, dok
administratorski VLAN zadržava puni pristup mreži.

---

## Mikrosegmentacija

Kao dodatni sigurnosni sloj implementirana je mikrosegmentacija na razini
serverskog sustava, čime je demonstriran višeslojni pristup sigurnosti.

---

## Zaključak

Provedeni projekt pokazao je kako VLAN segmentacija, u kombinaciji s ACL
pravilima i mikrosegmentacijom, značajno povećava sigurnost mrežnog
okruženja i smanjuje mogućnost širenja napada.
