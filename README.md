# Rekkiroikunta-ajastin

Yksinkertainen ajastin rekkitangossa roikkumisen harjoitteluun. Valittavat tavoiteajat: 0:30, 1:00, 1:30, 2:00, 2:30 ja 3:00.

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

Valitse ensin tavoiteaika yläreunan painikkeista: **0:30, 1:00, 1:30, 2:00, 2:30 tai 3:00**. Valinta jää muistiin selaimeen.

- Ajastin alkaa **-0:15**, jotta ehdit ottaa tangosta kiinni (3 viimeistä sekuntia piippaavat).
- **0:00** – huomioääni, aika alkaa juosta.
- **Joka 15. sekunti** – sama huomioääni.
- **Puolivälissä** – puheviesti ("Puoliväli, …") ja korostettu välähdys. Vain tavoitteilla 1:00 ja pidemmillä.
- **Viimeiset 5 sekuntia** – piippaava loppulaskenta.
- **Tavoiteaika** – aplodit + fanfaari + vihreä välähdys. Ajastin jatkaa bonusaikaa.

Napit: **KÄYNNISTÄ / PYSÄYTÄ / JATKA** ja **NOLLAA**.
Näppäimistöllä: `välilyönti` = käynnistä/pysäytä, `R` = nollaa, `1`–`6` = tavoiteaika.

Kaikki äänet tehdään selaimessa Web Audio APIlla, joten mukana ei ole äänitiedostoja.
Näyttö pidetään hereillä (Wake Lock) ajon aikana, jos selain tukee sitä.
