# Praktikum 10

**Praktikum 10 - ressursihaldus**
Praktikumi käigus õppisin ma paremini enda arvuti ressursse hallata ja nende tegevust kontrollida. Samuti tutvusin mitme erineva varem mulle tundmatu programmiga, mis võivad olla mul vajalikud, et arvutit paremini hallata.*


| Küsimus | Linux – vastus | Windows – vastus | Linuxi käsk | Windowsi tööriist |
|--------|-----------------|------------------|--------------|--------------------|
| Mitu protsessi kokku arvutis käib? | 254 | 327 | `ps aux \| wc -l` | Task Manager → Performance → CPU |
| Kõige esimesena käivitatud protsess | `PID 1: systemd` | `smss.exe` | `ps -eo pid,comm,lstart --sort=start_time` | Process Explorer → Start Time |
| Milliste kasutajate protsesse arvutis käib? | `niq, _chrony, avahi, colord, cups-br+, marcus-+, message+, polkitd, root, rtkit, syslog, systemd+` | `DWM-1, LOCAL SERVICE, marcus, NETWORK SERVICE, SYSTEM…` | `ps aux \| awk '{print $1}' \| sort \| uniq` | Task Manager → Details → User name |
| Arvuti uptime / viimati käivitatud | 41 min | 3 h 32 min | `uptime` | Task Manager → Performance → CPU |
| Kõige hiljem käivitatud protsess | `kworker/u24:4-e` | `imsctadn.exe` | `ps -eo pid,comm,lstart --sort=start_time` | Process Explorer → Start Time |
| Kõige rohkem CPU kasutav protsess | `gnome-shell ~0.6%` | `Spotify ~5%` | `top` | Task Manager → Processes → CPU |
| Kõige rohkem virtuaalmälu kasutav protsess | `gnome-shell VSZ=4603708` | `svchost.exe VSZ≈2 151 939 188 K` | `ps -eo vsz,comm --sort=-vsz` | Process Explorer → Virtual Size |
| Kõige rohkem füüsilist mälu kasutav protsess | `gnome-shell RSS=401260` | `chrome.exe ~400 MB` | `ps -eo rss,comm --sort=-rss` | Task Manager → Details → Working Set |
| Füüsilise mälu vaba ja hõivatud | Used: 1.3 GiB, Free: 6.4 GiB | In use: 13.9 GB, Available: 2 GB | `free -h` | Task Manager → Performance → Memory |
| Põhiketta vaba ruum | `/ = 82% vaba (~47G)` | `C: = 25% vaba (~120G)` | `df -h /` | C: → Properties |
| Kõige suurem fail ja kaust | Fail: `swap.img` (4.3G) <br> Kaust: `/usr` (4.0G) | Fail: `pagefile.sys` <br> Kaust: `C:\Users` | Fail: `sudo find / -xdev -type f -printf '%s %p\n' \| sort -nr \| head` <br> Kaust: `sudo du -xh --max-depth=1 / \| sort -h` | WinDirStat |
| sha1sum /dev/zero CPU alamtegevus | Enim: `us` (user) | – | `sha1sum /dev/zero \| sha1sum /dev/zero` + `top` | – |
| sha1sum /dev/urandom CPU alamtegevus | Enim: `sy` (system) | – | `sha1sum /dev/urandom \| sha1sum /dev/urandom` + `top` | – |
| Kõige rohkem kettale kirjutav protsess | – | System | – | Resource Monitor → Disk → Write |
| Fail, kuhu kirjutatakse kõige rohkem  | – | `C:\Windows\System32` | – | Resource Monitor → Disk Activity → Write |
| Kõige rohkem kettalt lugev protsess  | – | System | – | Resource Monitor → Disk → Read |
| Fail, kust loetakse kõige rohkem ( | – | `C:\Windows\Microsoft.NET\Framework64\v4.0.30319\clr.dll` | – | Resource Monitor → Disk Activity → Read |
| Suurima võrguliiklusega protsess  | – | `msedge.exe` <br> IP: 20.42.73.27 <br> Port: 60427 <br> Latency: 128 ms <br> Maht: 19 150 B | – | Resource Monitor → Network |

**Aeglane arvuti** :

Soovitaksin alguses vaadata Task Managerist (ctrl + shift + esc) vaadata Processes vaates CPU, Memory ja Disk veere, sorteerides need kahanevalt. CPU vaates otsi protsesse mis kasutavad pidevalt ule 60% CPU-d, Memory veerust vaata protsesse, mille Working Set on sellise programmi puhul väga suur pidevalt, näiteks mitu GB. Disk veerust vaata protsesse, mille Disk Active Time on 100% lähedane. Kui leidsid sealt midagi mainitud, siis uuri selle protsessi kohta ja vajadusel eemalda. Samuti võid soetada endale AutoRuns täienduse, kust saad vaadata, kas on sul arvutis kahtlaseid automaatselt käivituvaid programme, eriti .exe-d ja tundmatu publisheriga programmid. Vajadusel uuri ka nende kohta ja eemalda vajadusel. 


**Ekraanipildid:**


<img width="1281" height="879" alt="image" src="https://github.com/user-attachments/assets/030c6393-7a60-4fba-b591-44d40662c352" />
<img width="1911" height="1067" alt="image" src="https://github.com/user-attachments/assets/c2fe9481-3ecb-4395-8c4c-f7fd589e3c7a" />

# Lõpp
