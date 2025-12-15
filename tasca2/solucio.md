## Introducció
El client **Muntatges i Serveis Tècnics SL** necessita una política de còpies de seguretat robusta.  
S’han definit dues parts:  
1. Còpia de seguretat en un **equip Windows 11** amb Duplicati.  
2. Còpia de seguretat en un **servidor Ubuntu Linux** amb Duplicity i cron.  

---

## Part 1: Còpia de seguretat dels equips clients Windows

![Captura de la pàgina oficial](img/100.png)

Creació de la VM amb Windows 11
Es mostra la configuració inicial de la màquina virtual.  
**Per què?** Necessitem un entorn Windows per simular un client real.
  
  ![Captura de la pàgina oficial](img/img101.png)
  
  ![Captura de la pàgina oficial](img/img102.png)
  
  ![Captura de la pàgina oficial](img/img103.png)

Afegir un segon disc de 10 GB
Es veu com s’afegeix un disc addicional.  
**Per què?** Aquest disc simula el dispositiu local dedicat a còpies de seguretat
  
 ![Captura de la pàgina oficial](img/img105.png)

![Captura de la pàgina oficial](img/img106.png)

Instal·lació de Duplicati
Captures de la descàrrega i instal·lació.  
**Per què?** Duplicati és l’eina que permet fer còpies programades i xifrades
  
![Captura de la pàgina oficial](img/img107.png)

![Captura de la pàgina oficial](img/img108.png)

![Captura de la pàgina oficial](img/img109.png)

![Captura de la pàgina oficial](img/img110.png)

Primera execució de Duplicati
Es mostra la interfície web.  
**Per què?** Aquí es configuren els plans de còpia.

![Captura de la pàgina oficial](img/img111.png)

![Captura de la pàgina oficial](img/img112.png)

![Captura de la pàgina oficial](img/img113.png)

![Captura de la pàgina oficial](img/img114.png)

Configuració del destí de còpia (disc secundari)
Es defineix on es guardaran les còpies.  
**Per què?** Validem que el disc extra funciona com a repositori local.

![Captura de la pàgina oficial](img/img115.png)

![Captura de la pàgina oficial](img/img116.png)

![Captura de la pàgina oficial](img/img117.png)

![Captura de la pàgina oficial](img/img118.png)

Configuració del destí de còpia (Google Drive)
Es connecta amb un compte de Google Drive.  
**Per què?** Complim la regla 3-2-1: tenir una còpia fora de l’empresa.

![Captura de la pàgina oficial](img/img119.png)

![Captura de la pàgina oficial](img/img120.png)

![Captura de la pàgina oficial](img/img121.png)

![Captura de la pàgina oficial](img/img122.png)

---

# Part 2: Còpia de seguretat servidor Linux
![Captura de la pàgina oficial](img/ok1.png)

Detectar el disc nou amb lsblk
Es veu /dev/sdb de 10 GB.  
**Per què?** Identifiquem el disc on farem les còpies.

![Captura de la pàgina oficial](img/ok2.png)

Particionar amb parted
Es crea una partició XFS.  
**Per què?** Necessitem un sistema de fitxers robust per backups.

![Captura de la pàgina oficial](img/ok3.png)

Formatar amb mkfs.xfs
Es formata la partició.  
**Per què?** Preparar el disc per emmagatzemar dades.

![Captura de la pàgina oficial](img/ok4.png)

Muntar el disc a /media/backup
Es crea i munta el punt de muntatge.  
**Per què?** És el destí de les còpies.

![Captura de la pàgina oficial](img/ok5.png)

Instal·lació de duplicity i xfsprogs
Es confirma que els paquets estan instal·lats.  
**Per què?** Són les eines necessàries.

![Captura de la pàgina oficial](img/ok6.png)

![Captura de la pàgina oficial](img/ok7.png)

 Creació d’usuaris de prova (usuari1, usuari2)
Es creen comptes addicionals.  
**Per què?** Simulem un entorn multiusuari.

![Captura de la pàgina oficial](img/ok8.png)

![Captura de la pàgina oficial](img/ok9.png)

Creació de fitxers de prova amb fallocate
Es generen fitxers de 10 MB.  
**Per què?** Serviran per validar les còpies.

![Captura de la pàgina oficial](img/ok10.png)

Primera còpia completa amb duplicity
Es fa backup de /home.  
**Per què?** Punt de partida de la cadena de còpies.

![Captura de la pàgina oficial](img/ok11.png)

Restauració de fitxers
Es prova de restaurar fitxers esborrats.  
**Per què?** Validar que la còpia és usable.

![Captura de la pàgina oficial](img/ok12.png)

![Captura de la pàgina oficial](img/ok13.png)

Còpia incremental
Es crea un fitxer nou i es fa backup incremental.  
**Per què?** Comprovem que només es copien els canvis.

![Captura de la pàgina oficial](img/ok14.png)

![Captura de la pàgina oficial](img/ok15.png)

Estat de la col·lecció (collection-status)
Es mostra que hi ha còpia completa + incremental.  
**Per què?** Validació de la cadena de còpies.

![Captura de la pàgina oficial](img/ok16.png)

![Captura de la pàgina oficial](img/ok17.png)

Script fullbackup.sh
Es veu el contingut de l’script.  
**Per què?** Automatitza la còpia completa

![Captura de la pàgina oficial](img/ok18.png)

![Captura de la pàgina oficial](img/ok19.png)

Script incrementalbackup.sh
Es veu el contingut de l’script.  
**Per què?** Automatitza les còpies incrementals.

![Captura de la pàgina oficial](img/ok20.png)

![Captura de la pàgina oficial](img/ok21.png)

Configuració de cron
Es programen les execucions.  
**Per què?** Garantir còpies automàtiques cada dia.

![Captura de la pàgina oficial](img/ok22.png)

![Captura de la pàgina oficial](img/ok23.png)

Fitxers de backup al disc
Es mostren els .difftar.gpg i manifests.  
**Per què?** Evidència que les còpies s’han fet.

![Captura de la pàgina oficial](img/ok24.png)

![Captura de la pàgina oficial](img/ok25.png)

Comprovació amb collection-status
Es confirma la còpia completa i incremental.  
**Per què?** Validació final.

![Captura de la pàgina oficial](img/ok26.png)

Restauració puntual d’un fitxer
Es prova de recuperar fitxer1.bin.  
**Per què?** Validar restauració selectiva.



---

## Conclusions
- Amb Duplicity hem configurat còpies completes i incrementals al servidor Linux.  
- Els scripts garanteixen que la unitat de backup només estigui muntada durant la còpia.  
- Amb cron automatitzem el procés, assegurant còpies fiables cada dia.  

