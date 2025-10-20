# Praktikum 6 aruanne

Kuuenda praktikumi ülesanne oli:  "Protsessi signaalid, sisendid ja väljundid". Praktikumis õppisin ma rohkem protsesside signaalide, nende sisendite ja väljundite koht, näiteks kuidas neid neile saata erinevaid signaale ja kuidas modifitseerida väljundeid.

***Ülesanded***


**Ülesanne 1**
*Käivita gedit käsurealt, nüüd peata programmi töö ajutiselt klahvikombinatsiooniga CTRL+Z, veendu, et gediti aken on hangunud, seejärel saada talle SIGCONT-signaal ning veendu, et gediti aken toimib jälle. Pane oma aruandesse ekraanitõmmis käskude käivitamisest oma terminaliaknas.*

**Vastus**

<img width="1440" height="900" alt="ulesanne1-6" src="https://github.com/user-attachments/assets/fb07023b-5fbb-4149-be77-d79d9e0f689c" />

**Ülesanne 2**
*Käivita gedit taustal &-võtmega, saada sellele SIGHUP-signaal ja veendu, et aken sulgus. Seejärel käivita gedit nohup-käsuga, saada sellele uuesti SIGHUP-signaal ning veendu, et gedit jääb käima. Nüüd sisesta käsk, millega saad nohupi käivitatud gediti protsessi sulgeda. Pane oma aruandesse ekraanitõmmis käskude käivitamisest oma terminaliaknas, sh tõestuseks protsessi kadumise või allesjäämise kohta ps-käsu väljund.*

**Vastus**
![ulesanne_2-6](https://github.com/user-attachments/assets/a95fa4f9-6856-48f8-8eb8-08fbbf621eef)

**Ülesanne 3**
*Koosta ja lisa aruandesse käsujada, mis kuvab (modifitseerib) käsu ps -axu | grep daemon väljundi (ehk siis käsurea algus on fikseeritud) nii, et tulemuseks oleksid ainult programminimed koos lisaparameetritega*

**Vastus**
![ulesanne_3-6](https://github.com/user-attachments/assets/4d6741c7-af5e-4062-9e0f-a600161cc04a)

**Ülesanne 4**
*Koosta ja lisa aruandesse käsujada (ip a | grep ...| ... | cut ... jne), mis kuvab ekraanile vastuseks ainult arvuti IP-aadressi (enamasti 10.0.2.15) ip a-käsu väljundi põhjal.*

**Vastus**
![ulesanne_4-6](https://github.com/user-attachments/assets/f37fc9b9-a538-4a92-a6c0-99604ea1376a)


**Ülesanne 5**

 *Käivitage näidisprogramm WinTeated.exe ja tehke avanenud aknas erinevaid eriliigilisi tegevusi. Pange seejärel protsess kinni. Vaadake teatedOut.txt sisse ja tutvuge sõnumitega, mis Windows on saatnud antud protsessile. Valige juhuslikult 2 erinevat protsessile laekunud sõnumit ja otsige Interneti abiga ID-le vastav kirjeldus. Vähemalt 1 olgu selline, kus on parameetrid "wParam" ja/või "lParam" mitte nullid. Kirjeldage ja esitage aruandesse, mida kumbki sõnum ja parameetrid tähendavad (seehulgas mis tegevuse peale vastav sõnum saadeti protsessile). Proovige tekitada vähemalt 1 sõnum, mida pole tõlketabelis (failis teatedOut.txt on nimeks "???") ja ID on väiksem kui 45000. Millise(d) suutsite tekitada? Lisage ka lingid infoallikatele.*

 **Vastus**
 Valisin kaks protsessile laekunut sõnumit:
 31984;512;WM_MOUSEMOVE;144;1638478  --------- Tekkis, sest liigutasin hiirt programmiaknas. 81984 tähendab kaua programm töötas enne tegevust, 512- sõnumi ID, 144-Wparam, ütleb mis nupud olid liigutuse ajal all hoitud, WM_MOUSEMOVE - teate nimi, mis tähendab hiire liikumist aknas, 1638478 - lParam, sisaldab hiire kursiori x ja y kordinaate.https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-mousemove
 73010;274;WM_SYSCOMMAND;61472;65552  --------- 73010 tähendab kaua programm töötas enne tegevust, 274-sõnumi ID, WM_SYSCOMMAND- süsteemse tegevuse teade, 61472- Wparam, käsu kood, mis tähendab akna minimeerimist, 65552-lparam, hiirekursori kordinaadid x y, kust käsk tuli.

 # Lõpp

 
