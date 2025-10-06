# Praktikum 5 aruanne

Viienda praktikumi ülesanne oli:  " Failiõigused Linuxis". Praktikumis sai juhendi järgi lahendatud ära erinevaid ülesandeid, mis aitasid mul rohkem aru saada failiõiguste muutmisest ja nende toimimisest. 

***Ülesanded***

**Ülesanne 5-1**
*Katsetage missuguseid minimaalseid õigusi (r,w,x) on Unixis omanikul (u) vaja (/tmp/kaust - directory, minufail.txt - fail) (Grupile ja teistele ei anna mitte mingeid õiguseid). Minimaalsed õigused tuua välja eraldi nii kataloogi kui faili kohta:
a) kataloogis /tmp/kaust oleva faili minufail.txt lugemiseks?
b) kataloogis /tmp/kaust oleva faili minufail.txt kustutamiseks?*

**Vastus:**

a) Faili lugemiseks on vaja kataloogis õigust x ja failis õigus r.
b) Faili kustutamiseks on vaja ainult kataloogis õiguseid wx.

**Ülesanne 5-2**
*Miks chmod a=x skriptifail ei ole piisav õigus shelli skriptifaili käivitamiseks? Millist õigust lisaks käivitamisele veel vaja läheb skriptifaili käivitamiseks? Põhjendage lühidalt.*

**Vastus:**

Lisaks käivitamisõigusele on vajalik ka lugemisõigus ehk r, et shellil skripti sisu lugeda ja täita.

**Ülesanne 5-3**
*Milleks on kasulik see, et igal kasutajal on omanimeline grupp? (Teema: umask lõpp)*

**Vastus:**

See on kasulik, sest see aitab paremini õiguseid haldada ja on turvalisem, sest siis ei saa teised kasutajad vaikimisi kirjutada teise kasutaja failidesse.

**Ülesanne 5-4**
*Millised on minimaalsed õigused (rwx), mis on vajalikud teie tavakasutajal (kuulub gruppi majasisene) (mitte root- või peeter-kasutajal, kausta ja faili omanikud) faili uusfail.txt sisu kuvamiseks? Esitage ekraanivaade käskude id, ls -la ja cat uusfail.txt väljundist, tõestamaks lahendust.*

**Vastus:**

<img width="1440" height="900" alt="5-4" src="https://github.com/user-attachments/assets/d74681a8-fd22-4e11-b112-a0180d3c1f5f" />

**Ülesanne 5-5**
*Esitage kuvatõmmis tulemusest, kus oleks näha faili hinded.txt õigused ja jukuisa käivituskäsk koos väljundiga, ning lisage see oma esitusele. (Teema: setuid ja setgid.)*

**Vastus:**

<img width="1440" height="900" alt="5-5" src="https://github.com/user-attachments/assets/bd60ae46-5a33-428c-83d8-fa060ec7873c" />

**Ülesanne 5-6**
*Kas setuid kasutamine võib vähendada süsteemi turvalisust? Kui JAH, siis kuidas? Kui EI, siis miks ei vähenda?*

**Vastus:**

Jah, setuid võib vähendada turvalisust, sest see laseb tavalistel kasutajatel käivitada programme omaniku (näiteks rooti) õigustes, mis võib anda neile liigsed õigused ja võib viia turvaprobleemideni.

**Ülesanne 5-7**
*Kirjutage oma esitusele kõik kasutajad, kes saavad sticky bit-õigustega yhiskaust-kataloogist nüüd peeter-kasutaja loodud faile kustutada. (Teema: sticky bit)*

**Vastus:**

Sticky bit õigustega yhiskausta kataloogist saavad peetri loodud faile kustutada peeter ise, opetaja kuna ta on kataloogi omanik ja ka root kasutaja.

**Ülesanne 5-8**
*Uurige käsuga ls -la faili hinded.txt õigusi - mida märkate? Seejärel uurige õigusi täpsemalt, kasutades käsku getfacl ning kopeerige see tulemus oma esitusele. (teema: ACL)*

**Vastus:**

Sain sellise tulemuse:

#file: hinded.txt

#owner:opetaja

#group:opetaja

user::rw-

group:---

group:direktor:rw-

massk::rw-

other:---

**Ülesanne 5-9**
*Kes saab chattr +i-parameetriga faili sisu modifitseerida (kirjutada)? Milliste käskudega saate kustutada testfail-2-nimelise +i-parameetriga faili?*

**Vastus:**

Sellise parameetriga faili sisu modifitseerida saab ainult root kasutaja. Kustutada saab seda alles siis, kui eemaldad +i atribuudi käsuga sudo chattr -i testfail-2, see muudab faili jälle tavaliseks ja seda saab siis kustutada.


# **Lõpp**
