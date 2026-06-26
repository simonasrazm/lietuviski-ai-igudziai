# Mokymosi įrašo formatas

Mokymosi įrašai gyvena `./mokymosi-irasai/` ir naudoja nuoseklią numeraciją: `0001-pastabejimas.md`, `0002-pastabejimas.md` ir t. t. Katalogą sukurk tik tada, kai rašomas pirmasis įrašas (lazy).

Failai yra mokymosi atitikmenys ADR įrašams: fiksuoja neakivaizdžias pamokas, svarbias įžvalgas ir nurodytas išankstines žinias, kurios nustatys būsimas sesijas. Jie naudojami artimiausios raidos zonai apskaičiuoti.

## Šablonas

```md
# {Trumpas pavadinimas to, kas buvo išmokta ar nustatyta}

{1-3 sakiniai: kas buvo išmokta arba kokios išankstinės žinios buvo nustatytos, ir kodėl tai svarbu būsimoms sesijoms.}
```

Tai visas formatas. Mokymosi įrašas gali būti viena pastraipa. Vertė yra užfiksuoti, _kad_ tai dabar žinoma, ir _kodėl_ tai keičia, ko mokyti toliau - ne skyrių pildyme.

## Pasirenkami skyriai

Įtrauk juos tik tada, kai jie prideda tikros vertės. Daugumai įrašų jų nereikės.

- **Būsena** frontmatter (`aktyvus | atnaujinta LR-NNNN`) - naudinga, kai ankstesnis supratimas pasirodo klaidingas ir yra pakeičiamas.
- **Įrodymai** - kaip vartotojas parodė supratimą: atsakytas klausimas, atliktas pratimas, paminėta ankstesnė patirtis. Naudinga, kai teiginį gali reikėti peržiūrėti.
- **Pasekmės** - ką tai atrakina arba atmeta būsimoms sesijoms. Verta fiksuoti, kai tai neakivaizdu.

## Numeracija

Peržvelk `./mokymosi-irasai/`, rask didžiausią esamą numerį ir padidink vienetu.

## Kada rašyti mokymosi įrašą

Rašyk įrašą, kai teisingas bent vienas iš šių punktų:

1. **Vartotojas parodė tikrą supratimą apie netrivialų dalyką** - ne tik susipažino, bet yra įrodymų, kad gali sąvoką naudoti teisingai. Tai nustato naują bazę tam, ko mokyti toliau.
2. **Vartotojas atskleidė išankstines žinias** - „Aš jau žinau X.“ Užfiksuok tai, kad būsimos sesijos to nemokytų iš naujo. Taip pat užfiksuok nurodytą _gylį_.
3. **Klaidingas supratimas buvo pataisytas** - vartotojas anksčiau tikėjo kažkuo klaidingu, o dabar mato kodėl. Tai labai vertinga: prognozuoja būsimus užkliuvimus susijusioms temoms.
4. **Misija pasikoregavo dėl mokymosi** - vartotojas atrado, kad jam rūpi kažkas kita, nei manė. Susiek su [[MISIJA.md]] ir ją atnaujink.

### Kas _neatitinka_ kriterijų

- Medžiaga, kuri tik buvo aptarta. Aptarimas nėra mokymasis. Palauk įrodymų.
- Bet kas, kas jau glaustai užfiksuota [[ZODYNAS.md]] kaip termino apibrėžtis. Nedubliuok.
- Sesijų veiklos žurnalai. Mokymosi įrašai nėra dienoraštis - tai sprendimų lygio įžvalgos.

## Pakeitimas vėlesniu įrašu

Kai vėlesnis įrašas prieštarauja ankstesniam, nes vartotojo supratimas pagilėjo arba buvo pataisytas, pažymėk seną įrašą `Statusas: atnaujinta LR-NNNN`, o ne ištrink. Supratimo raidos istorija pati yra naudingas signalas.
