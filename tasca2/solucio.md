## Introducció
El client **Muntatges i Serveis Tècnics SL** necessita una política de còpies de seguretat robusta.  
S’han definit dues parts:  
1. Còpia de seguretat en un **equip Windows 11** amb Duplicati.  
2. Còpia de seguretat en un **servidor Ubuntu Linux** amb Duplicity i cron.  

---

## Part 1: Còpia de seguretat dels equips clients Windows

### Creació de la màquina virtual
- Crear una VM amb Windows 11 i dos discos (un per al sistema i un secundari de 10 GB).
- 
  ![Captura de la pàgina oficial](img/100.png)
  
  ![Captura de la pàgina oficial](img/img101.png)
  
  ![Captura de la pàgina oficial](img/img102.png)
  
  ![Captura de la pàgina oficial](img/img103.png)
  
- **Per què?** El segon disc simula un dispositiu local dedicat a còpies de seguretat.

### Instal·lació de Duplicati
- Descarregar i instal·lar [Duplicati]

    **![Captura de la pàgina oficial](img/img105.png)

  ![Captura de la pàgina oficial](img/img106.png)
  
- **Per què?** És una eina gratuïta que permet fer còpies locals i al cloud amb programació horària.

![Captura de la pàgina oficial](img/img107.png)

![Captura de la pàgina oficial](img/img108.png)

![Captura de la pàgina oficial](img/img109.png)

![Captura de la pàgina oficial](img/img110.png)

![Captura de la pàgina oficial](img/img111.png)

![Captura de la pàgina oficial](img/img112.png)

![Captura de la pàgina oficial](img/img113.png)

![Captura de la pàgina oficial](img/img114.png)

![Captura de la pàgina oficial](img/img115.png)

![Captura de la pàgina oficial](img/img116.png)

![Captura de la pàgina oficial](img/img117.png)

![Captura de la pàgina oficial](img/img118.png)

![Captura de la pàgina oficial](img/img119.png)

![Captura de la pàgina oficial](img/img120.png)

![Captura de la pàgina oficial](img/img121.png)

![Captura de la pàgina oficial](img/img122.png)


### Configuració del pla de còpies
- Crear dos plans de còpia:  
  - Cada hora → disc secundari.  
  - A les 18:00 → Google Drive (amb un compte específic).
  -
  - - **Per què?** Això segueix l’esquema **3-2-1**: 3 còpies, 2 suports diferents, 1 còpia fora de l’empresa.

### Validació del funcionament
- Afegir arxius a **Documents** i comprovar que es copien.  
- Esborrar Documents i restaurar des del disc secundari.  
- Restaurar també des de Google Drive.
  
- **Per què?** Validem que les còpies i restauracions funcionen correctament.

---

# Part 2: Còpia de seguretat servidor Linux
![Captura de la pàgina oficial](/img/ok2.png)

![Captura de la pàgina oficial](/img/ok3.png)

![Captura de la pàgina oficial](/img/ok4.png)

![Captura de la pàgina oficial](/img/ok5.png)

![Captura de la pàgina oficial](/img/ok6.png)

![Captura de la pàgina oficial](/img/ok7.png)

![Captura de la pàgina oficial](/img/ok8.png)

![Captura de la pàgina oficial](/img/ok9.png)

![Captura de la pàgina oficial](/img/ok10.png)

![Captura de la pàgina oficial](/img/ok11.png)

![Captura de la pàgina oficial](/img/ok12.png)

![Captura de la pàgina oficial](/img/ok13.png)

![Captura de la pàgina oficial](/img/ok14.png)

![Captura de la pàgina oficial](/img/ok15.png)

![Captura de la pàgina oficial](/img/ok16.png)

![Captura de la pàgina oficial](/img/ok17.png)

![Captura de la pàgina oficial](/img/ok18.png)

![Captura de la pàgina oficial](/img/ok19.png)

![Captura de la pàgina oficial](/img/ok20.png)

![Captura de la pàgina oficial](/img/ok21.png)

![Captura de la pàgina oficial](/img/ok22.png)

![Captura de la pàgina oficial](/img/ok23.png)

![Captura de la pàgina oficial](/img/ok24.png)

![Captura de la pàgina oficial](/img/ok25.png)

![Captura de la pàgina oficial](/img/ok26.png)



---

## Conclusions
- Amb Duplicity hem configurat còpies completes i incrementals al servidor Linux.  
- Els scripts garanteixen que la unitat de backup només estigui muntada durant la còpia.  
- Amb cron automatitzem el procés, assegurant còpies fiables cada dia.  

