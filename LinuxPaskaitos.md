#- Paskaita 1

#- Paskaita 2

#- Paskaita 3

	vi redaktorius ir jo pagrindinės komandos

vi – tai teksto redaktorius, dažniausiai įdiegtas UNIX operacinėse sistemose. Juo patogu rašyti
skriptus ar reikiamą tekstą. Viena išskirtinių jo ypatybių yra tai, jog ši programa reaguoja į klaviatūra
įvedamas komandas, ir būtent jų pagalba galima redaguoti tekstą. vi turi du veikimo režimus:
įvesties, kai galima įvesti norimus simbolius, rašyti, ir redagavimo, kai failą galima koreguoti (ištrinti,
pakeisti) ar ieškoti eilutės, jį išsaugoti ir pan. Dirbant su vi svarbu nesupainioti jo veikimo režimų ir
atkreipti dėmesį į įvedamas komandų didžiąsias ir mažąsias raides – taip galima išvengti klaidų ir
nepatogumų.

Pagrindinės komandos:

Failo sukūrimas, peržiūra:

vi <failas>	 terminale įvykdyta komanda sukuria/atidaro failą vi redaktoriuje
cat <failas>	 terminale išspausdina failo turinį
less <failas>	 terminale išspausdina failo turinį puslapiais

Failo redagavimas:

i	 įjungia teksto įvedimo režimą: įvedamas tekstas prieš žymeklį
I	 įjungia teksto įvedimo režimą: įvedamas tekstas eilutės pradžioje
O	 įjungia teksto įvedimo režimą: įvedamas tekstas virš eilutės
o	 įjungia teksto įvedimo režimą: įvedamas tekstas po eilute
esc	 išjungia teksto įvedimo režimą, įjungia redagavimo režimą
r	 pakeičia vieną simbolį ties žymekliu
R	 pakeičia simbolius ties žymekliu (kol paspaudžiamas esc)

„Keliavimas“ faile:

j, k, h, l arba rodyklių klavišai	 leidžia su žymekliu (kursoriumi) judėti faile
^	 žymeklį grąžiną į eilutės pradžią
$	 žymeklį nusiunčia į eilutės pabaigą
nG	 žymeklį nusiunčia į n-tąją eilutę
G	 žymeklį nusiunčia į paskutinę eilutę
w	 žymeklį nusiunčia į kito žodžio pradžią
nw	 žymeklį nusiunčia n žodžių į priekį
b	 žymeklį grąžiną į prieš tai esančio žodžio pradžią

nb	 žymeklį nusiunčia n žodžių atgal
:set nu	 sunumeruoja failo eilutes
/<eilutė> tekste ieško <eilutė> žemiau nuo žymeklio
?<eilutė> tekste ieško <eilutė> aukščiau nuo žymeklio

Turinio trynimas:

x	 ištrina vieną simbolį
nx	 ištrina n simbolių
dd	 ištrina vieną eilutę
u	 pataiso vieną keitimą (panaikina koregavimą)
U	 pataiso visus keitimus vienoje eilutėje

Failo išsaugojimas:

ZZ	 išsaugo failą ir jį išjungia
:q!	 neišsaugo paskutinių keitimų ir išjungia failą
:w	 išsaugo failą
:wq	 išsaugo failą ir jį išjungia

Šaltiniai:
https://www.guru99.com/the-vi-editor.html
https://ryanstutorials.net/linuxtutorial/vi.php
https://www.cs.colostate.edu/helpdocs/vi.html

#- Paskaita 4

#- Paskaita 5

#- Paskaita 6
	
	Git sistema

	Git yra versijų kontrolės sistema, kuri leidžia patogiai vystyti programinę įrangą koordinuojant programų kūrėjų darbą bei parodant failų keitimus. Git daugiausia naudojama programinės įrangos kūrimui, tačiau į talpyklą galima įdėti įvairius failus, juos keisti ir tvarkyti. Vienas pagrindinių šios sistemos privalumų – keli žmonės, dirbantys prie vieno projekto, gali efektyviai dirbti atskirai ir sujungti savo darbo rezultatus į vieną bendrą rezultatą, netrukdydami vienas kitam, neatlikdami perteklinių užduočių ir pan. Taip pat naudojantis šia sistema lengva atsekti visus talpykloje įvykdytus pokyčius, juos atitaisyti ir pan., dar ji yra greito veikimo.

Sistema yra pagrįsta paskirstytomis talpyklomis. Vartotojas gali sukurti talpyklą ir joje saugoti savo failus. Šią talpyklą galima persikopijuoti į kitą kompiuterį, taisyti ar papildyti joje esančius failus, juos registruoti į vietinę talpyklą, o galiausiai išsaugoti pagrindinėje talpykloje, taip atliekant pakeitimus pagrindinėje šakoje. Kadangi talpykloje galima sukurti atskiras šakas, galima turėti kelias failo versijas, o tai patogu išbandant skirtingus variantus ar prie vienos užduoties dirbant keliese.

Talpyklą į kompiuterį nukopijuoti galima naudojant komandą „git clone“. Tuomet į kompiuterį nukopijuojami visi talpykloje esantys failai. Galima atlikti jų pakeitimus, sukurti naujus failus ir pan., tada šiuos pakeitimus vietinėje talpykloje išsaugo komanda „git add“. Galiausiai į serverį pakeitimus įrašo komanda „git push“. Vienais atvejais įvairūs failo pakeitimai yra suderinami su originaliu failu, tad vykdant atitinkamas komandas skirtingos šakos yra sklandžiai sujungiamos į vieną, kitais atvejais taip neįvyksta, nes sistema nežino, kuria versija vadovautis ir kaip derėtų jas sujungti, tuomet konfliktus išspręsti prašoma paties vartotojo.
