# Rekkiroikunta-ajastin

Yksinkertainen ajastin rekkitangossa roikkumisen harjoitteluun. Tavoite: 2 minuuttia.

## Käyttö

Avaa `index.html` selaimessa – ei asennusta, ei riippuvuuksia.

```
open index.html
```

Jos haluat käyttää sitä puhelimella samassa wifissä, käynnistä kevyt palvelin:

```
python3 -m http.server 8000
```

ja avaa puhelimen selaimessa `http://<koneen-ip>:8000`.

## Toiminta

- Ajastin alkaa **-0:15**, jotta ehdit ottaa tangosta kiinni (3 viimeistä sekuntia piippaavat).
- **0:00** – piippaus, aika alkaa juosta.
- **0:15** – korostettu välähdys + merkkiääni + puhe.
- **Jokainen 15 sekunnin väli** (0:30, 0:45, 1:15, 1:45) – sama huomioääni kuin lähdössä.
- **1:00** – korostettu välähdys + sointu.
- **1:30** – korostettu välähdys + sointu ("enää 30 sekuntia").
- **1:55–1:59** – loppukirin laskenta.
- **2:00** – aplodit + fanfaari + vihreä välähdys. Ajastin jatkaa bonusaikaa.

Napit: **KÄYNNISTÄ / PYSÄYTÄ / JATKA** ja **NOLLAA**.
Näppäimistöllä: `välilyönti` = käynnistä/pysäytä, `R` = nollaa.

Kaikki äänet tehdään selaimessa Web Audio APIlla, joten mukana ei ole äänitiedostoja.
Näyttö pidetään hereillä (Wake Lock) ajon aikana, jos selain tukee sitä.
