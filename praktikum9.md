 # Praktikum 9


| Küsimus | Windows | Windowsi kasutatud töörist | Linux | Linuxi käsk
| --- | --- | --- | --- | --- |
| Mitu protsessi kokku arvutis käib? | 129-131 | Win + X -> Tegumihaldur -> Jõudlus | 253 | ps aux \| wc -l |
| Milline on kõige esimesena käivitatud protsess?  | smss.exe | Käsuviip -> tasklist | /sbin/init splash | ps aux --sort=start_time \| head -n 2 |
| Milliste kasutajate protsesse arvutis käib? | Lev | Tegumihaldur -> Kasutajad | lev root avahi syslog message+ systemd+ | ps aux	 |
| Kui kaua on arvuti järjest töötanud (up time)? | 0:00:10:17 | Tegumihaldur -> Jõudlus | 13:15:17 up 9 min,  1 user | uptime |
| Milline protsess käivitati kõige hiljem (viimasena)? | tasklist.exe | Käsuviip -> tasklist | /lib/systemd/ | ps aux --sort=-start_time |
| Milline on kõige rohkem protsessoriaega võttev protsess ja kui mitu protsenti protsessoriajast ta tarbib? | Süsteemi jõuduoleku protsess / 97% | Tegumihaldur -> Üksikasjad -> CPU | systemd-oomd | top |
| Milline on kõige rohkem virtuaalmälu (aadressiruumi, commit, Virtual Size) võttev protsess? | firefox.exe | Tegumihaldur -> Üksikasjad -> Mälu | gnome-shell | top-m |
| Milline on kõige rohkem füüsilist mälu (working set) võttev protsess? | firefox.exe | Tegumihaldur -> Üksikasjad -> Töökomplekt (mälu) | gnome-shell | top -o RES |
| Kui palju füüsilisest mälust (Physical Memory) on vaba ja kui palju hõivatud? | 2,3GB kasutatud ja 2,5GB vaba | Tegumihaldur -> Jõudlus -> Mälu | 1,7GB | free -h |
| Kui palju on põhikettal (C:, /) vaba ruumi mahult (GB) ja protsentuaalselt? | 21,02GB 33% | Win + X -> Kettahaldus | 14GB 45% | df -h |
| Milline on kõige suurem arvutis olev fail ja kõige rohkem andmemahtu hõivav kaust (arvesse võta ka alamkaustade mahtu, ja jätta juurkaust / või C: välja)? | Nextcloud-3.14.3-x64.msi / Lenght: 160935936 bites ja kaust Downloads | Powershell -> Get-ChildItem -Path . -Recurse  Where-Object { -not $_.PSIsContainer }  Sort-Object Length -Descending  Select-Object FullName, Length -First 1  / Get-ChildItem -Path . -Directory -Recurse  ForEach-Object { $_  Add-Member -MemberType NoteProperty -Name Size -Value (Get-ChildItem -Path $_.FullName -Recurse  Where-Object { -not $_.PSIsContainer }  Measure-Object -Property Length -Sum).Sum; $_ } Sort-Object Size -Descending  Select-Object FullName, Size -First 1 | Kaust: /home/lev Fail: ./snap/firefox/common/ .cache/mozilla/firefox /20lmd57f.default/cache2/entries/ CD1919CFFD6A82DA4D61359AF100488A4328AD6B | Fail: find -type f -exec du -h {} + \| sort -rh \| head -n 1 Alamkaust:du -h --max-depth=1 /home/lev \| sort -rh \| head -n 2 |
| Võrrelge terminali käskude: sha1sum /dev/zero sha1sum /dev/zero ja sha1sum /dev/urandom sha1sum /dev/urandom protsessori kasutust. |  | | pilt allpool, mõlemad käsud crash'isid terminali | |
| Milline protsess kõige rohkem salvestusseadmele kirjutab? Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab? Milline protsess kõige rohkem salvestusseadmelt loeb? Millisest failist eelmise küsimuse protsess kõige rohkem loeb? | 1. msedge.exe 2. C\Users\Lev\AppData/Local\Microsoft\Edge\User Data/Default\uu_hot_config 3. svcchsot.exe 4. C:\Windows\System32\winevt\Logs\Security.evtx | 1. Ressursimonitor -> Ketas -> Kettategevus -> Kirjutamine 2. Ressursimonitor -> Ketas -> Kettategevus -> Fail 3. Ressursimonitor -> Ketas -> Kettategevus -> Lugemine  4. Ressursimonitor -> Ketas -> Kettategevus -> Fail | | |
| Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga?  | Suurima mahuga võrguliikluse on tekitanud protsess nextcloud.exe, mille kogumaht on 144 B/sek. | | | |
| Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutad põhjustaja tuvastamiseks.  | `htop` - jälgige protsesse, mis tarbivad palju ressursse, nagu CPU või mälu. `ps aux` - kuvage protsessid, mis võtavad palju CPU- või mäluruumi. `top` - sorteerige protsessid CPU või mälu kasutuse järgi. | | | |



![image](https://github.com/user-attachments/assets/72fd3f1b-5a7c-4cba-88f8-431b73240ca7)

![image](https://github.com/user-attachments/assets/1b639720-0a91-42c4-9a8a-71e90219c797)


