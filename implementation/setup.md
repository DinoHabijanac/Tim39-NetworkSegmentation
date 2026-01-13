# Upute za postavljanje i pokretanje projekta

## Preduvjeti
Za pokretanje i pregled ovog projekta potrebno je imati instaliran sljedeći alat:

- **Cisco Packet Tracer** (verzija 8.0 ili novija)

## Preuzimanje projekta
Projekt se može preuzeti kloniranjem GitHub repozitorija ili preuzimanjem ZIP
arhive s GitHuba.

Primjer kloniranja repozitorija pomoću Gita:

```bash
git clone https://github.com/DinoHabijanac/Tim39-NetworkSegmentation
```

## Pokretanje projekta

1. Pokrenuti aplikaciju **Cisco Packet Tracer**
2. Otvoriti datoteku:
```bash
implementation/src/Network_segmentation_example01.pkt
```
4. Nakon otvaranja projekta učitat će se mrežna topologija s konfiguriranim
VLAN-ovima, rutiranjem i ACL pravilima.

---

## Testiranje funkcionalnosti

Ispravnost konfiguracije može se provjeriti izvođenjem sljedećih testova:

- Ping testovi između krajnjih uređaja unutar istog VLAN-a
- Ping testovi između uređaja u različitim VLAN-ovima
- Testiranje HTTP prometa iz Users VLAN-a prema Servers VLAN-u

### Očekivano ponašanje mreže

- Komunikacija unutar istog VLAN-a je dopuštena
- ICMP promet iz Users VLAN-a prema ostalim VLAN-ovima je blokiran
- HTTP promet iz Users VLAN-a prema Servers VLAN-u je dopušten
- Management VLAN ima puni pristup svim mrežnim segmentima

---

## Napomena

Projekt je izrađen u edukacijske svrhe i služi za demonstraciju osnovnih
principa mrežne segmentacije, VLAN konfiguracije i kontrole prometa primjenom
ACL pravila u simuliranom laboratorijskom okruženju.


