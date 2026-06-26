# ADR formatas

ADR įrašai gyvena `docs/adr/` ir naudoja nuoseklią numeraciją: `0001-irasas.md`, `0002-irasas.md` ir t. t.

Sukurk `docs/adr/` katalogą tik tada, kai reikia pirmo ADR.

## Šablonas

```md
# {Trumpas sprendimo pavadinimas}

{1-3 sakiniai: koks kontekstas, ką nusprendėme ir kodėl.}
```

Tai visas formatas. ADR gali būti viena pastraipa. Vertė yra užfiksuoti, kad sprendimas priimtas ir kodėl, o ne užpildyti daug skyrių.

## Pasirenkami skyriai

Įtrauk tik tada, kai jie prideda tikros vertės. Daugumai ADR jų nereikės.

- **Statusas** frontmatter (`pasiulyta | priimta | nebeaktualu | atnaujininta ADR-NNNN`) - naudinga, kai sprendimai peržiūrimi
- **Svarstytos alternatyvos** - tik kai atmestas alternatyvas verta prisiminti
- **Pasekmės** - tik kai reikia įvardyti neakivaizdžius tolesnius padarinius

## Numeracija

Peržvelk `docs/adr/`, rask didžiausią esamą numerį ir padidink vienetu.

## Kada siūlyti ADR

Visi trys punktai turi būti teisingi:

1. **Sunku pakeisti** - vėliau pakeisti nuomonę būtų reikšmingai brangu
2. **Stebina be konteksto** - būsimas skaitytojas žiūrės į kodą ir klaus „kodėl taip padaryta?“
3. **Tikras kompromisas** - buvo realių alternatyvų ir viena pasirinkta dėl aiškių priežasčių

Jei sprendimą lengva atšaukti, praleisk. Jei jis nestebina, niekas neklaus kodėl. Jei nebuvo tikros alternatyvos, nėra ko fiksuoti, išskyrus „padarėme akivaizdų dalyką“.

### Kas tinka

- **Architektūrinė forma.** „Naudojame monorepo.“ „Rašymo modelis yra event-sourced, skaitymo modelis projektuojamas į Postgres.“
- **Integracijų tarp kontekstų modeliai.** „Užsakymai ir Apmokestinimas bendrauja per domeno įvykius, ne sinchroninį HTTP.“
- **Technologijų pasirinkimai, kurie sukuria prisirišimą.** Duomenų bazė, žinučių brokeris, autentifikacijos tiekėjas, diegimo taikinys.
- **Ribų ir apimties sprendimai.** „Kliento duomenys priklauso Kliento kontekstui; kiti kontekstai juos nurodo tik pagal ID.“
- **Sąmoningi nukrypimai nuo akivaizdaus kelio.** „Naudojame rankinį SQL vietoj ORM, nes X.“
- **Apribojimai, nematomi kode.** „Negalime naudoti AWS dėl atitikties reikalavimų.“ „Atsakymo laikas turi būti mažesnis nei 200 ms dėl partnerio API sutarties.“
- **Atmestos alternatyvos, kai atmetimas neakivaizdus.** Jei svarstei GraphQL ir pasirinkai REST dėl subtilių priežasčių, užfiksuok tai.
