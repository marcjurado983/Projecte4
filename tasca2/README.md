# T02: DPR: còpies de seguretat. Cas pràctic
[solucio de la tasca](solucio.md)

## 📝 Introducció al cas
A la tasca anterior es va dissenyar una política de còpies de seguretat pel client **Muntatges i Serveis Tècnics SL**. Ara toca portar a la pràctica l’estudi i elaborar guies tècniques amb proves de concepte perquè el personal pugui implantar el pla de còpies de seguretat.

---

## 🔹 Part 1: Còpia de seguretat dels equips clients Windows

Encara que inicialment no es contemplava fer còpia dels arxius locals, s’ha fet una excepció amb l’equip **Windows 11** del director de l’empresa.  
Aquest equip conté informació sensible que no es vol al servidor de fitxers. Per això es defineix una política de còpies seguint l’esquema **3-2-1**:

- Una còpia al **disc secundari local** (10 GB).  
- Una còpia al **cloud (Google Drive)** amb l’eina **Duplicati**.  

### 🔧 Prova de concepte
1. Crear una màquina virtual Windows 11 amb dos discos (sistema + secundari 10 GB).  
2. Instal·lar **Duplicati**.  
3. Configurar còpies del perfil d’usuari:  
   - Cada hora → disc secundari.  
   - A les 18:00 → Google Drive.  
4. Afegir arxius a Documents i comprovar còpies.  
5. Esborrar Documents i restaurar des del disc secundari.  
6. Fer una restauració des de la còpia al cloud.  

---

## 🔹 Part 2: Còpia de seguretat servidor Linux

Per al servidor Linux s’utilitza **Duplicity**, que permet còpies locals o remotes. Amb **cron** es poden automatitzar les polítiques de còpia.

### 🔧 Prova de concepte
1. Crear una màquina virtual **Ubuntu Server** amb un segon disc de 10 GB.  
2. Inicialitzar i formatar en **xfs**, muntar a `/media/backup`.  
3. Instal·lar **duplicity**.  
4. Crear usuaris addicionals i arxius de prova (4 arxius de 10 MB).  
5. Fer còpia de seguretat de `/home`.  
6. Esborrar arxius i restaurar-los.  
7. Afegir un arxiu nou de 4 MB i fer còpia incremental.  
8. Desmuntar la unitat de backup.  

### 🔧 Automatització amb scripts
- **fullbackup.sh**  
  - Fa còpia completa de `/home` al volum muntat.  
  - Usa la variable d’entorn `PASSPHRASE`.  
  - Programat amb cron els **diumenges a les 23:00**.  

- **incrementalbackup.sh**  
  - Fa còpies incrementals de `/home`.  
  - Usa la mateixa passphrase.  
  - Programat amb cron de **dilluns a dissabte a les 23:00**.  

---

## ✅ Conclusions
Amb aquesta prova de concepte s’ha demostrat:
- La viabilitat de l’esquema **3-2-1** en Windows amb Duplicati.  
- La integració de **Duplicity + cron** en Linux per còpies completes i incrementals.  
- La importància de mantenir la unitat de backup desmuntada per seguretat.  

Aquestes guies permeten al client implantar un sistema de còpies robust i escalable.

