---
name: suplanuok-ir-aprasyk
description: Planavimo klausimų sesija, kuri tikrina planą pagal projekto (programavimo) kalbą ir dokumentuotus sprendimus, tikslina terminus ir prireikus atnaujina CONTEXT.md bei ADR įrašus. Naudok, kai vartotojas nori patikrinti planą prieš projekto taksonimiją, srities modelį ar esamus architektūrinius sprendimus.
---

<ka-daryti>

Atkakliai apklausk mane apie kiekvieną šio plano aspektą, kol pasieksime bendrą supratimą. Eik per sprendimų medžio šakas po vieną, aiškindamasis priklausomybes tarp sprendimų. Prie kiekvieno klausimo pateik savo rekomenduojamą atsakymą.

Klausk po vieną klausimą ir palauk atsakymo prieš tęsdamas.

Jei į klausimą galima atsakyti patyrinėjus kodą ar darbo erdvę, pirmiausia patyrinėk kodą ar darbo erdvę.

</ka-daryti>

<papildoma-informacija>

## Domeno suvokimas

Tyrinėdamas kodą, ieškok ir esamos dokumentacijos.

### Failų struktūra

Dauguma repozitoriumų turi vieną kontekstą:

```text
/
├── CONTEXT.md
├── docs/
│   └── adr/
│       ├── 0001-event-sourced-orders.md
│       └── 0002-postgres-for-write-model.md
└── src/
```

Jei šaknyje yra `CONTEXT-MAP.md`, repozitoriumas turi kelis kontekstus. Žemėlapis parodo, kur jie yra:

```text
/
├── CONTEXT-MAP.md
├── docs/
│   └── adr/                          ← visos sistemos sprendimai
├── src/
│   ├── ordering/
│   │   ├── CONTEXT.md
│   │   └── docs/adr/                 ← konkretaus konteksto sprendimai
│   └── billing/
│       ├── CONTEXT.md
│       └── docs/adr/
```

Failus kurk tik tada, kai turi ką įrašyti. Jei nėra `CONTEXT.md`, sukurk jį tada, kai išsprendžiamas pirmas terminas. Jei nėra `docs/adr/`, sukurk katalogą tada, kai prireikia pirmo ADR.

## Sesijos metu

### Tikrink pagal žodyną

Kai vartotojas vartoja terminą, kuris kertasi su esama kalba `CONTEXT.md`, iškart tai įvardyk. Pavyzdys: „Žodyne 'atšaukimas' apibrėžtas kaip X, bet dabar atrodo, kad turi omenyje Y. Kuris variantas teisingas?“

### Tikslinink miglotą kalbą

Kai vartotojas vartoja neaiškius ar nevinareikšmius terminus, pasiūlyk tikslų etaloninį terminą. Pavyzdys: „Sakai 'paskyra' - ar turi omenyje klientą, ar vartotoją? Tai skirtingi dalykai.“

### Aptark konkrečius scenarijus

Kai kalbama apie srities ryšius, tikrink juos konkrečiais scenarijais. Sugalvok kraštutinius atvejus, kurie verčia tiksliai apibrėžti ribas tarp sąvokų.

### Lygink su kodu

Kai vartotojas teigia, kaip kažkas veikia, patikrink, ar programinis kodas sutampa. Jei randi prieštaravimą, parodyk jį: „Kodas atšaukia visą užsakymą, bet ką tik sakei, kad galimas dalinis atšaukimas. Kuris variantas teisingas?“

### Atnaujink CONTEXT.md iškart

Kai terminas išsprendžiamas, iškart atnaujink `CONTEXT.md`. Nekaupk pakeitimų vėlesniam laikui. Naudok formatą iš [CONTEXT-FORMAT.md](./CONTEXT-FORMAT.md).

`CONTEXT.md` neturi turėti įgyvendinimo detalių. Nenaudok `CONTEXT.md` kaip specifikacijos, juodraščio ar įgyvendinimo sprendimų vietos. Tai yra žodynas ir niekas daugiau.

### ADR siūlyk taupiai

Siūlyk kurti ADR tik tada, kai teisingi visi trys punktai:

1. **Sunku pakeisti** - vėliau pakeisti nuomonę būtų reikšmingai brangu
2. **Stebina be konteksto** - būsimas skaitytojas klaustų „kodėl taip padaryta?“
3. **Tikras kompromisas** - buvo realių alternatyvų ir viena pasirinkta dėl aiškių priežasčių

Jei bent vieno punkto nėra, ADR praleisk. Naudok formatą iš [ADR-FORMAT.md](./ADR-FORMAT.md).

</papildoma-informacija>

