# Praktikum 9


| Küsimus | Windows | Windowsi kasutatud töörist | Linux | Linuxi käsk
| --- | --- | --- | --- | --- |
| Mitu protsessi kokku arvutis käib? | 129-131 | Win + X -> Tegumihaldur -> Jõudlus | | |
| Milline on kõige esimesena käivitatud protsess?  | smss.exe | Käsuviip -> tasklist | | |
| Milliste kasutajate protsesse arvutis käib? | Lev | Tegumihaldur -> Kasutajad | | |
| Kui kaua on arvuti järjest töötanud (up time)? | 0:00:10:17 | Tegumihaldur -> Jõudlus | | |
| Milline protsess käivitati kõige hiljem (viimasena)? | tasklist.exe | Käsuviip -> tasklist | | |
| Milline on kõige rohkem protsessoriaega võttev protsess ja kui mitu protsenti protsessoriajast ta tarbib? | Süsteemi jõuduoleku protsess / 97% | Tegumihaldur -> Üksikasjad -> CPU | | |
| Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess? | firefox.exe | Tegumihaldur -> Üksikasjad -> Mälu | | |
| Kui palju füüsilisest mälust (Physical Memory) on vaba ja kui palju hõivatud? | 2,3GB kasutatud ja 2,5GB vaba | Tegumihaldur -> Jõudlus -> Mälu | | |
| Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? | 21,02GB 33% | Win + X -> Kettahaldus | | |
| Milline on kõige suurem arvutis olev fail ja kõige rohkem andmemahtu hõivav kaust (arvesse võta ka alamkaustade mahtu, ja jätta juurkaust / või C: välja)? | Nextcloud-3.14.3-x64.msi / Lenght: 160935936 bites ja kaust Downloads | Powershell -> Get-ChildItem -Path . -Recurse | Where-Object { -not $_.PSIsContainer } | Sort-Object Length -Descending | Select-Object FullName, Length -First 1 | | |
| Võrrelge terminali käskude: sha1sum /dev/zero | sha1sum /dev/zero ja sha1sum /dev/urandom | sha1sum /dev/urandom protsessori kasutust. | | | | |
| | | | | |
| | | | | |
| | | | | |


| | | | | |




| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |
