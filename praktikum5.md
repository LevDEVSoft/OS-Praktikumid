# Praktikum 5 - Failiõigused Linuxis


5.1. Minimaalsed vajalikud õigused:

a) Faili lugemiseks peab olema lugemisõigus.

b) Faili kustutamiseks peab olema kirjutamis- ja kustutamisõigus.
5.2. Käsk "chmod a=x" annab kõigile kasutajatele käivitusõiguse, kuid faili käivitamiseks on vaja nii lugemis- kui ka käivitusõigust. Seetõttu peaks faili käivitamiseks olema määratud vähemalt "chmod a=rx".

5.3. See lihtsustab gruppidepõhist koostööd, võimaldab failide juurdepääsu paremat kontrollimist ja tugevdab süsteemi turvalisust.

5.4 ![image](https://github.com/user-attachments/assets/2a45cd01-7c63-4772-b492-78363cc3e91f)



# file: hinded.txt
# owner: opetaja
# group: opetaja
user::rw-
group::---
other::---
