# Legalize LT

### Lietuvos teisės aktai Markdown formatu, versijuojami su Git.

Kiekvienas teisės aktas yra failas. Kiekviena reforma yra commit'as.

**14,945 teisės aktai** · **71,794 commit'ai** · Atviri duomenys iš data.gov.lt

Projekto [Legalize](https://github.com/legalize-dev/legalize) dalis · [legalize.dev](https://legalize.dev)

> **Ankstyva stadija** — Šis repozitorijus yra aktyviai vystomas. Failų struktūra, commit'ų istorija ir turinys gali būti reikšmingai keičiami, įskaitant pilną pergeneravimą.

## Greita pradžia

```bash
# Klonuoti Lietuvos teisės aktus
git clone https://github.com/legalize-dev/legalize-lt.git

# Lietuvos Respublikos Konstitucijos 1 straipsnis
grep -A 3 "1 straipsnis" lt/TAR.47BB952431DA.md

# Konkretaus teisės akto istorija
git log --oneline -- lt/TAR.8A39C83848CB.md
```

## Struktūra

```
lt/
  TAR.47BB952431DA.md  — Lietuvos Respublikos Konstitucija
  TAR.8A39C83848CB.md  — Civilinis kodeksas
  TAR.65AD818F5F9C.md  — Civilinio proceso kodeksas
  ...                  — 14,945 teisės aktai
```

Teisės akto rūšis (konstitucija, įstatymas, kodeksas, konstitucinis įstatymas) nurodyta YAML antraštėje kiekviename faile, ne katalogų struktūroje.

## Formatas

Kiekvienas failas turi:

- **YAML frontmatter** — metaduomenys: pavadinimas, dokumento ID, data, statusas, rūšis, TAR kodas, šaltinis
- **Markdown tekstas** — konsoliduotas teisės akto tekstas su skirsnių ir straipsnių struktūra

Commit'ai naudoja istorinę kiekvieno pakeitimo paskelbimo datą. Kiekviename commit'e yra trailer'iai su teisės akto ir pakeitimo identifikatoriais, leidžiantys rekonstruoti pilną teisės aktų istoriją su `git log`.

### Versijų istorija

Kiekvienos teisės akto versijos pilnas tekstas (Suvestinė) yra fetch'inamas iš data.gov.lt Suvestine lentelės. Konstitucija turi 12 versijų (1992-2022), Civilinis kodeksas turi 100 versijų (2004-2026).

## Šaltinis

Duomenys gaunami iš:

- [data.gov.lt Spinta API](https://get.data.gov.lt/datasets/gov/lrsk/teises_aktai/) — Lietuvos atvirų duomenų portalas
- Originalus šaltinis: [e-tar.lt](https://www.e-tar.lt) — Teisės aktų registras

## Padėka

- **[data.gov.lt](https://data.gov.lt/)** — už visų Lietuvos teisės aktų pateikimą atvirais duomenimis su Spinta API
- **[Teisės aktų registras (TAR)](https://www.e-tar.lt/)** — už oficialų Lietuvos teisės aktų registrą

## Licencija

Teisės aktų tekstai yra vieši dokumentai. Struktūrizavimas ir formatavimas pagal [MIT](LICENSE) licenciją.

---

Sukūrė [Enrique Lopez](https://enriquelopez.eu) · [legalize.dev](https://legalize.dev)
