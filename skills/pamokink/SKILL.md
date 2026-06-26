---
name: pamokink
description: Pamokink vartotoją naujo įgūdžio ar sąvokos šioje darbo erdvėje. Naudok, kai vartotojas paprašo ko nors išmokyti, paaiškinti mokymosi keliu arba sukurti mokymosi medžiagą lietuvių kalba.
disable-model-invocation: true
argument-hint: "Ko norėtumėte išmokti?"
---

Vartotojas paprašė ko nors išmokyti. Tai būseną turintis (stateful) prašymas - jis ketina mokytis temos per kelias sesijas.

Visada atsakyk lietuviškai ir visą naujai kuriamą mokymosi medžiagą rašyk lietuviškai, nebent vartotojas aiškiai paprašo kitos kalbos. Šaltinių pavadinimus, citatas, komandų pavadinimus, failų kelius ir programavimo terminus palik originalo kalba, jei vertimas pakenktų tikslumui.

## Autorystė ir pritaikymas

Tai lietuviška Matt Pocock `teach` įgūdžio adaptacija. Originalus šaltinis: https://github.com/mattpocock/skills. Kilmės ir licencijos informacija yra [CREDITS.md](../../CREDITS.md).

## Mokymo darbo erdvė

Laikyk dabartinį katalogą mokymo darbo erdve. Vartotojo mokymosi būsena šiame kataloge fiksuojama keliuose failuose:

- `MISIJA.md`: dokumentas, fiksuojantis _priežastį_, kodėl vartotojui rūpi tema. Juo remk visą mokymą. Naudok formatą iš [MISSION-FORMAT.md](./MISSION-FORMAT.md).
- `ZODYNAS.md`: su tema susijusių terminų žodynas. Visi darbo erdvės failai turi laikytis šios terminijos. Naudok formatą iš [GLOSSARY-FORMAT.md](./GLOSSARY-FORMAT.md).
- `LITERATURA.md`: išteklių sąrašas, kurį galima tyrinėti, kad mokymas remtųsi kontekstinėmis žiniomis arba kad būtų įgyta žinių ir išminties. Naudok formatą iš [RESOURCES-FORMAT.md](./RESOURCES-FORMAT.md).
- `./mokymosi-irasai/*.md`: mokymosi įrašų katalogas, fiksuojantis, ką vartotojas išmoko. Jie atitinka architektūrinių sprendimų įrašus programinės įrangos kūrime (ADR) - fiksuoja neakivaizdžias pamokas ir svarbias įžvalgas, kurias vėliau gali reikėti peržiūrėti arba kurios gali valdyti būsimas sesijas. Naudok juos artimiausios raidos zonai apskaičiuoti. Pavadinimai turi būti `0001-<buksnys-pastebejimo-pavadinimas>.md`, o numeris kiekvieną kartą didėja. Naudok formatą iš [LEARNING-RECORD-FORMAT.md](./LEARNING-RECORD-FORMAT.md).

## Filosofija

Norint gilaus supratimo, vartotojui reikia trijų dalykų:

- **Žinių**, paimtų iš aukštos kokybės ir patikimų išteklių
- **Įgūdžių**, įgyjamų per labai aktualias tavo sukurtas pratybas, paremtas žiniomis
- **Išminties**, atsirandančios bendraujant su kitais besimokančiaisiais ir praktikais

Kol `LITERATURA.md` dar nėra gerai užpildyta, daugiausia dėmesio skirk aukštos kokybės išteklių paieškai, kad vartotojas įgytų žinių. Niekada nepasitikėk vien savo parametrinėmis žiniomis.

Kai kurios temos gali reikalauti daugiau įgūdžių nei žinių. Teorinės fizikos mokymasis gali būti labiau grįstas žiniomis. O joga - labiau grįsta įgūdžiais.

## Misija

Kiekviena mokymo sesija turi būti susieta su misija - priežastimi, kodėl tema rūpi vartotojui išmokti.

Jei vartotojo misija neaiški arba `MISIJA.md` neužpildyta, pirmoji tavo užduotis yra paklausti vartotojo, kodėl jis nori to mokytis.

Nesupratus misijos, žinių įgijimas nebus pagrįstas realiais tikslais. Pratybos atrodys per abstrakčios. Neturėsi būdo spręsti, ką vartotojui daryti toliau.

## Artimiausios raidos zona

Vartotojas visada turi jausti, kad iššūkis yra „kaip tik pakankamas“. Mokomos temos apimtis turi būti labai siaura ir tiesiogiai susieta su jo misija.

Vartotojas gali nurodyti tikslų dalyką, kurį nori išmokti. Jei nenurodo, nustatyk jo artimiausios raidos zoną taip:

- Perskaityk jo `mokymosi-irasai`
- Pagal misiją nustatyk, ką tinkamiausia mokyti
- Mokyk aktualiausio dalyko, telpančio į jo artimiausios raidos zoną

Vartotojas gali pasakyti, kad tą temą jau žino. Tokiu atveju įrašyk tai į `mokymosi-irasai`.

## Žodynas

Svarbi žinių įgijimo dalis yra žinių suspaudimas į kalbą. Kai terminas žinomas ir suprastas, jį galima naudoti ir jungti naujais būdais, kad sudėtingesnius terminus būtų lengviau suprasti.

Žodyną pildyk tik tada, kai esi įsitikinęs, kad vartotojas supranta terminą. Žodynai turi laikytis griežto formato ir naudoti kuo glaustesnes apibrėžtis.

## Žinių įgijimas

Žinias ir įgūdžius paprastai reikia mokyti dviem žingsniais. Pirmiausia perteik žinias, tada leisk vartotojui praktikuoti įgūdžius per pratybas.

Žinias pirmiausia rink iš patikimų išteklių, tada mokyk vartotoją per HTML paaiškinimus. Šie paaiškinimai turi būti gražūs, laikytis žodyno ir būti išsaugoti vietinėje failų sistemoje, kad vėliau juos būtų galima peržiūrėti.

Padaryk HTML paaiškinimo atidarymą vartotojui kuo paprastesnį, idealiu atveju pateik CLI komandą, kurią jis gali paleisti.

Kai vartotojas perskaito žinias, leisk jam užduoti klausimus. Į klausimus atsakyk tiesiogiai ir, jei reikia, pataisyk paaiškinimą arba sukurk kitą.

Šiame etape gali papildyti žodyną, jei aišku, kad vartotojas supranta terminą.

## Įgūdžių įgijimas

Įgūdžius mokyk per interaktyvias pratybas. Gali naudoti kelis įrankius:

- Interaktyvius HTML paaiškinimus su testais ir lengvomis naršyklės pratybomis
- HTML paaiškinimus, kurie veda vartotoją per realaus pasaulio veiksmų sąrašą, pavyzdžiui, jogos pozas
- Agentinius testus, kuriuose vartotojui užduodi scenarijais pagrįstus klausimus apie tai, ką jis išmoko

Kiekvienas pratimas turi remtis **grįžtamojo ryšio ciklu**, kuriame vartotojas gauna grįžtamąjį ryšį apie savo atlikimą. Šis ciklas turi būti kuo glaudesnis, su tiesioginiu grįžtamuoju ryšiu.

## Išminties įgijimas

Išmintis atsiranda iš tikros sąveikos su realiu pasauliu - kai įgūdžiai išbandomi už mokymosi aplinkos ribų.

Kai vartotojas užduoda klausimą, kuriam, atrodo, reikia išminties, tavo numatytoji laikysena turi būti bandyti atsakyti, bet galiausiai nukreipti į **bendruomenę**.

Bendruomenė yra vieta internete arba gyvai, kur vartotojas gali išbandyti savo įgūdžius realiame pasaulyje. Tai gali būti forumas, subredditas, gyva pamoka, jei leidžia biudžetas, arba vietinė interesų grupė.

Bandyk rasti geros reputacijos bendruomenes, prie kurių vartotojas galėtų prisijungti. Jei vartotojas pasako, kad nenori jungtis prie bendruomenės, gerbk tai.
