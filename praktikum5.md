# Praktikum 5 - Failiõigused Linuxis


5.1. Minimaalsed vajalikud õigused:

a) Faili lugemiseks peab olema lugemisõigus.

b) Faili kustutamiseks peab olema kirjutamis- ja kustutamisõigus.

5.2. Käsk "chmod a=x" annab kõigile kasutajatele käivitusõiguse, kuid faili käivitamiseks on vaja nii lugemis- kui ka käivitusõigust. Seetõttu peaks faili käivitamiseks olema määratud vähemalt "chmod a=rx".

5.3. See lihtsustab gruppidepõhist koostööd, võimaldab failide juurdepääsu paremat kontrollimist ja tugevdab süsteemi turvalisust.

5.4 ![image](https://github.com/user-attachments/assets/2a45cd01-7c63-4772-b492-78363cc3e91f)

Minimaalsed õigused, et tavakasutaja (grupis majasisene) saaks faili uusfail.txt sisu kuvada, on järgmised:

Kaustal: r-x (lugemis- ja täitmisõigused, et liikuda kausta ja näha faile).
Failil: r-- (lugemisõigus, et faili sisu kuvada).

5.6:
Jah, setuid kasutamine võib vähendada süsteemi turvalisust, sest programm, millel on setuid, jookseb faili omaniku õigustes. Kui programm sisaldab haavatavusi, võib pahatahtlik kasutaja saada kõrgendatud õigused ja pääseda ligi süsteemi ressurssidele, millele tal muidu juurdepääsu poleks.

(Setuid- ja setgid-bittide tüüpiline käitumine UNIX-i keskkonnas kujutab endast tuntud turvaprobleemi. Ründaja võib ära kasutada setuid- ja setgid-bittide käitumist, kirjutades täidetava faili üle näiteks "trooja" viirusega ja käivitades seejärel faili. Täidetav fail käivitatakse omaniku õigustega, mitte ründaja õigustega.)

5.7
Sticky bit-õigustega kaustast saab peeter-kasutaja loodud faile kustutada:

Peeter ise (faili omanik).
Õpetaja
Kausta omanik.
Root-kasutaja (süsteemi administraator).

5.8:
Kui uurida käsuga ls -la faili hinded.txt õigusi, märkad tavalisi failisüsteemi õigusi (nt -rw-r--r--). Kasutades käsku getfacl, näed lisaks standardsetele õigustele ka ACL õigusi, mis annavad failile paindlikumad juurdepääsu reeglid, näiteks grupipõhised õigused.

#file: hinded.txt

#owner: opetaja

#group: opetaja

user::rw-

group::---

other::---

5.9:
Ainult root või kasutaja, kes määras failile +i (immutable) parameetri, saab faili muuta või eemaldada. Et kustutada +i-parameetriga faili, tuleb esmalt eemaldada +i atribuut.


## screenshottid:


![Screenshot 2024-10-21 163826](https://github.com/user-attachments/assets/ec7684e8-e188-4648-9956-8a316b9b3608)
![Screenshot 2024-10-21 171827](https://github.com/user-attachments/assets/80c9bb0f-32bd-4d01-9d1a-d61bf728b484)
