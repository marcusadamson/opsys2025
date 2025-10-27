# Praktikum 7 aruanne

Kuuenda praktikumi ülesanne oli:  "Haakimine". Praktikumis õppisin ma kuidas Linuxis ja Windowsis andmekandjaid mountida.

***Ülesanded***

1 ja 2  *Miks uued andmekandjad vajavad lähtestamist? (Täpseid vastuse nõudeid vaata ülesande juurest).*

**Vastus**

Uus andmekandja ei ole kohe kasutamiseks valmis, operatsioonisusteem ei oska seda lugeda, kuna sellel puudub partitsioonitabel ja failisüsteem. Lähtestamine loob andmekandjale struktuuri , mis ütleb arvutile, kuidas ketast kasutada ja kuhu andmeid salvestada. Ilma selleta ei oska operatsioonisüsteem seadet lugeda ega kirjutada.

Erinevused GPTl ja MBR-il

1) GPT suudab hallata üle 2 TB mahuga andmekandjaid, MRB piirang on 2TB

2) GPT võimaldab kuni 128  partitsiooni, MBR aga nelja.

3) GPT salvestab partitsioonitabeli metaandmed nii ketta algusesse kui lõppu, pakkudes varukoopiat ja suuremat tõrketaluvust.

4) Igal partitsioonil GPT-l on unikaalne GUID, mis välistab konfliktid ja teeb partitsioonide haldamise automaatsemaks. MRB-l aga pole.


3.  *Lisage link https://kodu.ut.ee/~TÜ_kasutajatunus/opsys/hdd.png praktikumi aruandesse tõestuseks, et olete ülesande TÜ võrguketta haakimine Windowsis edukalt lahendanud.*

**Vastus**

https://kodu.ut.ee/~marcusadamson/opsys/hdd.png

4. *Lisage käsu ls -la /mnt/ut/public_html/opsys/ väljundi pilt aruandesse.*

   **Vastus**

<img width="1440" height="900" alt="praktikum7-hdd_ubuntus" src="https://github.com/user-attachments/assets/86a55e19-e24d-4149-8281-80e7cd47fc08" />

5. *Mida mõjutasid mount-käsu parameetrid -o ro ja -t auto?*

**Vastus**

-o ro paneb andmekandja ainult lugemiseks, nii et saab faile vaadata, aga mitte muuta. -t auto tähendab, et Ubuntu otsib ise välja, mis failisüsteem pulgal on ja valib selle järgi õige ühenduse viisi.

6. Leidke mount-käsu väljundist üles, mis väärtusega asendas Ubuntu auto-parameetri.

   **Vastus**
   
   Asendas parameetriga ISO9600

8. Tehke ekraanipilt /etc/fstab-faili sisust pärast iseseisva ülesande lahendamist (või muu tõestus, et 4 TB ketas haagitaks Ubuntu käivitamisel automaatselt kausta /mnt/bigdata).

   **Vastus**
   <img width="1440" height="900" alt="dwawda" src="https://github.com/user-attachments/assets/fc320e00-d72f-41f3-900f-0ca71f7fbcee" />


# Lõpp




