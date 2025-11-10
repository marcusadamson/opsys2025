# Praktikum 9- Teenused ja optimeerimine

**Selles praktikumis õppisin ma rohkem keskkonnamuutujatest, süsteemi optimeerimisest ja erinevatest teenustest ja nende vajalikusest. Tööks kulus mul umbes 6 tundi, kuna sattusin tehniliste probleemide otsa**

**Ülesanded**

Ülesanne 1: Sisestage operatsioonisüsteemid Ubuntu 25.04 terminali käsk sudo su ja vajadusel andke käsule lisaks teie kasutaja parool. Nüüd tuvastage käsureal PWD keskkonnamuutuja väärtus ja lisage see aruandesse tekstikujul.

*Vastus*

PWD keskkonnamuutuja väärtus sudo su käsu puhul oli PWD= /home/marcus ja sudo su - puhul PWD= /root

Ülesanne 2: Sisestage käsureale käsud alias ja aeg. Esitage väljundist ekraanivaade juhendisse. Väljundis peaks olema selgelt näha aliased aeg, inf_cpu, inf_memory ja aeg aliase väjundina juhendis eelnevalt defineeritud spetsiifilise kujuga kuupäev ja kellaaeg.

*Vastus*

<img width="1440" height="900" alt="PRAK9-2" src="https://github.com/user-attachments/assets/be4e709e-2553-445c-9c84-e554be8d9d28" />

Ülesanne 3: Vaata paigaldatud tarkvara nimekirja ja leia midagi, mis tundub olema üleliigne. Otsi selle kohta lisainfot, et mis on antud tarkvara funktsioon ja teiseks miks ta ebavajalik (vajadused võivad olla inimestel erinevad). Esitada põhjendus, vabastatud kettamaht ja ekraanipilt, et olete eemaldanud enda valitud tarkvara (näha eemaldamise käsud ja vahetult kohe käsk dpkg -l | grep minuValitudEemaldatudTarkvara).

*Vastus*

Thunderbird on Mozilla loodud e-posti klient ja kuna mina kasutan e-posti veebibrauseris, siis mul ei ole seda vaja. Vabastatud kettamaht on 72,7kb

<img width="1440" height="900" alt="prak_8-3" src="https://github.com/user-attachments/assets/ed02d262-ef44-4e1c-8aae-1b07d52f5866" />

Ülesanne 4: Tehke kuvatõmmis "dir" käsust ja oma valitud EXE-faili käivitamisest, et oleks näha programmi käivitumine (sh ei ole järgmisel real veateadet vmt). (teema Windows keskkonnamuutujad)

*Vastus*

<img width="858" height="520" alt="image" src="https://github.com/user-attachments/assets/ab34babf-8afa-4ed1-af83-82e9886b405b" />


Ülesanne 5: Kui käivitatav fail leidub nii kasutaja kui ka süsteemi "%Path%" märgitud kaustades ja need kaustad on erinevad, siis kummas kataloogis olev fail käivitatakse?

*Vastus*
Kui käivitatav fail asub nii kasutaja kui ka süsteemi %Path% kataloogides, siis käivitatakse kasutaja %Path%-is olev fail.

Ülesanne 6: Võta teenuste loendist teenus, mille teenuse nimi algab oma perenime esitähega (ÕÄÖÜ puhul võta teenused algustähega C, Q, W, X, Y) (teenuste nimedes jäta "Windows" või "Microsoft" eest ära ehk "Windows Time" loeme "Time" oma nimede esitähtede järgi teenuseid valides). Kirjuta eelnevalt valitud teenuse kohta otstarve. Teiseks, kas teenuse töötamine on vajalik oma masinas (ja miks) (kas võib teenuse "disabled" määrata)?

*Vastus*

🔹 Teenuse nimi:

AppX Deployment Service (AppXSvc)

🔹 Otstarve:

AppX Deployment Service on Microsofti süsteemne teenus, mis haldab Windowsi Store ja AppX rakendusi.

🔹 Kas teenuse töötamine on vajalik?

See on vajalik, kui kasutad Windows Store-i ja selle poolt saadud rakendusi, muidu ei ole. Siiski pärast eemaldamist taastasin selle.

Ülesanne 7: Anna käsk (asenda "Microsoft.People" oma välja valitud tarkvarapakiga) Get-AppxPackage -Name "Microsoft.People" | select packageFullName. Seejärel anna eemaldamise käsk ja kohe peale eemaldamist uuesti eelpool toodud käsk (Get-AppxPackage ...). Esita sellest kuvatõmmis.

*Vastus*

<img width="1913" height="1078" alt="image" src="https://github.com/user-attachments/assets/5020eb87-6310-4503-8aa9-0914e4276b60" />



Ülesanne 8: Esitage hostnamectl käsu väljundi ekraanivaade teie Ubuntu virtuaalmasinast, mis on uuendatud Ubuntu 25.10 versioonile.

*Vastus*

<img width="1276" height="881" alt="image" src="https://github.com/user-attachments/assets/ddd4082c-3b4b-4ce2-907a-5b4867ed2dff" />

# Lõpp

