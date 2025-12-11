GUIA DE TOT EL PROCEDIMENT DE Accés remot. Escriptori remot (RDP)

![Captura de la pàgina oficial](img/img1.png)

![Captura de la pàgina oficial](img/img2.png)

Què fem: Al client Linux fem ping 10.0.2.15 i al Windows ipconfig per veure la IP.

Perquè: Confirmem que hi ha connectivitat entre les dues màquines.

![Captura de la pàgina oficial](img/img3.png)

Què fem: Obrim Configuració → Sistema → Escritorio remoto i activem RDP.

Perquè: Sense activar-lo, el servidor no acceptaria connexions.

![Captura de la pàgina oficial](img/img4.png)

Què fem: agreguem un usuari per el remot

Perquè: per establir la connexió.

![Captura de la pàgina oficial](img/img5.png)

Què fem: Obrim la finestra “Seleccionar usuaris” i afegim l’usuari local Marc.

Perquè: Donem permisos a l’usuari correcte.


![Captura de la pàgina oficial](img/img6.png)

Què fem: Es mostra la llista d’usuaris amb accés remot.

Perquè: Validem que els permisos estan configurats.

![Captura de la pàgina oficial](img/img7.png)

Què fem: Apareix un avís de certificat (Marc.local) i es pregunta si volem acceptar-lo.

Perquè: El certificat és auto-generat i cal acceptar-lo per continuar.

![Captura de la pàgina oficial](img/img8.png)

Què fem: Introduïm usuari i contrasenya per accedir via RDP.

Perquè: RDP requereix credencials per seguretat.

![Captura de la pàgina oficial](img/img9.png)

![Captura de la pàgina oficial](img/img10.png)

Què fem: Es mostra la sessió de Windows 11 Enterprise des del client.

Perquè: Confirmem que la connexió RDP funciona.


![Captura de la pàgina oficial](img/img11.png)

![Captura de la pàgina oficial](img/img12.png)

Què fem: A Zorin configurem Remote Desktop amb el nom del dispositiu i l’adreça (ms-rd://usuari12-VirtualBox.local).

Perquè: Així establim la connexió des de Linux cap a Windows.


![Captura de la pàgina oficial](img/img14.png)

Què fem: Es mostra la finestra per escriure credencials (usuari12, contrasenya).

Perquè: Validem l’accés amb credencials correctes.

![Captura de la pàgina oficial](img/img15.png)

Què fem: Apareix un avís dient que el certificat no és de confiança.

Perquè: Cal acceptar-lo per establir la connexió.

![Captura de la pàgina oficial](img/img16.png)

Què fem: Es confirma que la connexió RDP és funcional i segura.

Perquè: Demostra que podem donar suport gràfic a l’usuari final.
