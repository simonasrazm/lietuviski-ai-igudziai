# CONTEXT.md formatas

## Struktūra

```md
# {Konteksto pavadinimas}

{Vieno ar dviejų sakinių aprašymas, kas yra šis kontekstas ir kodėl jis egzistuoja.}

## Kalba

**Užsakymas**:
{Vieno ar dviejų sakinių termino aprašymas}
_Vengti_: Pirkimas, transakcija

**Sąskaita faktūra**:
Prašymas apmokėti, siunčiamas klientui po pristatymo.
_Vengti_: Sąskaita, mokėjimo prašymas

**Klientas**:
Asmuo arba organizacija, pateikianti užsakymus.
_Vengti_: Pirkėjas, paskyra
```

## Taisyklės

- **Turėk poziciją.** Kai tai pačiai sąvokai yra keli žodžiai, pasirink geriausią ir kitus išvardyk kaip vengtinus sinonimus.
- **Žymėk aiškiai konfliktus.** Jei terminas vartojamas dviprasmiškai, įrašyk jį į „Pažymėtos dviprasmybės“ su aiškiu sprendimu.
- **Laikyk glaustus apibrėžimus.** Daugiausia vienas ar du sakiniai. Apibrėžk, kas terminas yra, o ne ką jis daro.
- **Rodyk ryšius.** Naudok paryškintus terminų pavadinimus ir aiškiai įvardyk kardinalumą, kai jis akivaizdus.
- **Įtrauk tik šiam projekto kontekstui būdingus terminus.** Bendros programavimo sąvokos nepriklauso šiam failui, net jei projektas jas plačiai naudoja. Prieš pridėdamas terminą paklausk: ar tai šiam kontekstui unikali sąvoka, ar bendras programavimo konceptas?
- **Grupuok po poskyriais**, kai natūraliai atsiranda terminų grupės. Jei visi terminai priklauso vienai sričiai, tinka ir plokščias sąrašas.
- **Parašyk dialogo pavyzdį.** Trumpas programuotojo ir srities eksperto pokalbis turi parodyti, kaip terminai natūraliai sąveikauja ir kur yra ribos tarp panašių sąvokų.

## Vieno ir kelių kontekstų repozitoriumai

**Vienas kontekstas:** vienas `CONTEXT.md` repozitoriumo šaknyje.

**Keli kontekstai:** `CONTEXT-MAP.md` repozitoriumo šaknyje išvardija kontekstus, jų vietas ir tarpusavio ryšius:

```md
# Kontekstų žemėlapis

## Kontekstai

- [Užsakymai](./src/ordering/CONTEXT.md) - priima ir seka klientų užsakymus
- [Apmokestinimas](./src/billing/CONTEXT.md) - generuoja sąskaitas faktūras ir apdoroja mokėjimus
- [Vykdymas](./src/fulfillment/CONTEXT.md) - valdo sandėlio surinkimą ir siuntimą

## Ryšiai

- **Užsakymai → Vykdymas**: Užsakymai skleidžia `OrderPlaced` įvykius; Vykdymas juos naudoja surinkimui pradėti
- **Vykdymas → Apmokestinimas**: Vykdymas skleidžia `ShipmentDispatched` įvykius; Apmokestinimas juos naudoja sąskaitoms faktūroms generuoti
- **Užsakymai ↔ Apmokestinimas**: Bendri `CustomerId` ir `Money` tipai
```

Įgūdis pats nustato, kuri struktūra galioja:

- Jei yra `CONTEXT-MAP.md`, perskaityk jį, kad rastum kontekstus
- Jei yra tik šakninis `CONTEXT.md`, tai vienas kontekstas
- Jei nėra nei vieno, sukurk šakninį `CONTEXT.md` tik tada, kai išsprendžiamas pirmas terminas

Kai yra keli kontekstai, nustatyk, su kuriuo susijusi dabartinė tema. Jei neaišku, paklausk.
