# Studentų rezultatų analizės programa (v0.4)

Programa skirta studentų duomenų apdorojimui. Ji gali:

- generuoti studentų failus su atsitiktiniais pažymiais
- nuskaityti studentų duomenis iš failo
- apskaičiuoti galutinį balą
- surūšiuoti studentus pagal pasirinktą kriterijų
- padalinti studentus į dvi grupes:
  - vargšiukai (galutinis < 5.0)
  - galvočiai (galutinis ≥ 5.0)
- išvesti rezultatus į naujus failus

## Programos struktūra

Projektas suskirstytas į kelis failus:

- main.cpp – pagrindinė programos logika
- studentas.h – Studentas struktūra
- skaiciavimai.cpp / .h – galutinio balo ir medianos skaičiavimas
- ivestis.cpp / .h – įvesties validacija
- isvesti.cpp / .h – rezultatų spausdinimas
- generavimas.cpp / .h – failų generavimas

## Sugeneruoti duomenų failai

Programos testavimui buvo sugeneruoti šie failai:

| Failas | Studentų skaičius |
|------|------|
| studentai1000.txt | 1 000 |
| studentai10000.txt | 10 000 |
| studentai100000.txt | 100 000 |
| studentai1000000.txt | 1 000 000 |
| studentai10000000.txt | 10 000 000 |

## 1 tyrimas – failų generavimo sparta, kai ND kiekis = 3

Buvo matuojamas laikas, reikalingas sugeneruoti studentų failus.

## 2 tyrimas – duomenų apdorojimo sparta, kai ND kiekis = 3 ir rušiuojama pagal rezultatą

Buvo matuojamas:

- failo nuskaitymo laikas
- rūšiavimo laikas
- studentų skirstymo laikas
- rezultatų įrašymo laikas
- bendras programos veikimo laikas

## Rezultatų analizė

Didėjant studentų skaičiui programos veikimo laikas proporcingai didėja. 
Didžiausią dalį vykdymo laiko užima duomenų nuskaitymas ir rūšiavimas.

Failų generavimas taip pat tampa žymiai lėtesnis su labai dideliais duomenų kiekiais.

## Programos paleidimas

Programa kompiliuojama:

g++ -O2 main.cpp skaiciavimai.cpp ivestis.cpp isvesti.cpp generavimas.cpp -o programa

Paleidimas:

./programa

## Rezultatų nuotraukos

https://media.discordapp.net/attachments/912454523077935144/1482028146441326662/Screenshot_2026-03-13_165023.png?ex=69b575c4&is=69b42444&hm=d633f18dea471f1dcdc43f76ff28ce727e7465736054fd59fd4f349ab257ea06&=&format=webp&quality=lossless&width=1371&height=221

https://media.discordapp.net/attachments/912454523077935144/1482029272922194010/image.png?ex=69b576d1&is=69b42551&hm=0450ef0d123313a049b8db7cfcfb2f26956603a1b6674c8117189bea4ed92138&=&format=webp&quality=lossless&width=1095&height=930