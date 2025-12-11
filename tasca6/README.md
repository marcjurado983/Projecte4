# T06: Accés remot. Escriptori remot (RDP) (tasca individual)
[solucio de la tasca](solucio.md)

## 📌 Introducció
En la tasca anterior vam establir les bases de l'administració remota de servidors mitjançant la línia de comandes (**SSH**).  
Però, què passa quan el servidor que administrem és un **Windows Server amb interfície gràfica**?  
O, més important encara, què passa quan un client ens truca i diu:  
- "No em funciona el programa X"  
- "M'ha sortit un error a la pantalla"  

Com a consultors d’**EverPia**, no només gestionem backend, sinó que donem suport directe a l’usuari final.  
No n’hi ha prou amb una terminal; necessitem **veure el que ells veuen i prendre el control del seu ratolí i teclat**.

---

## 🎯 Missió: Guies de Suport Gràfic (PoC)
La tasca és crear la **documentació oficial** que rebran els futurs becaris per a tasques de suport remot.  
Farem una **Prova de Concepte (PoC)** interna utilitzant màquines virtuals per crear les guies d’ús sobre com establir connexions d’**Escriptori Remot**.

---

## 🖥️ Tecnologia predominant
- **RDP (Remote Desktop Protocol):**  
  L’estàndard de Microsoft per administrar equips Windows.  
  Actualment, RDP també està disponible en entorns **GNU/Linux (Gnome)**, de manera que podem connectar-nos des d’un **Zorin OS** a un **Windows 11** amb la mateixa facilitat.

---

## 📂 Fase 1: Anàlisi comparativa i selecció
1. Investigar quatre alternatives populars d’assistència remota:  
   - TeamViewer  
   - AnyDesk  
   - Google Remote Desktop  
   - Una quarta eina escollida per vosaltres  

2. Crear una **taula comparativa** amb criteris clau:  
   - Facilitat d’ús (client)  
   - Disponibilitat (Windows, macOS, Linux)  
   - Model de preu (llicència, limitacions)  

3. Presentar una **recomanació oficial**: escollir l’eina més adequada per EverPia.

---

## 📂 Fase 2: Creació de les guies d’ús

### 📘 Guia 1: Manual per al tècnic (intern EverPia)
- **Instal·lació** de la versió completa/tècnica de l’eina.  
- **Inici d’una sessió de suport.**  
- **Gestió de funcions clau:**  
  - Transferència d’arxius  
  - Canvi de pantalla/multi-monitor  
  - Reinici remot  
- **Bones pràctiques de seguretat:**  
  - Tancar sempre la sessió  
  - No desar contrasenyes de clients  
  - Documentar la incidència  

---

### 📗 Guia 2: Manual per al client (usuari final)
- **Descàrrega del mòdul QuickSupport (o equivalent).**  
- Instruccions pas a pas amb captures:  
  - Obrir el fitxer.  
  - Localitzar ID i contrasenya.  
  - Comunicar l’ID al tècnic.  
  - Acceptar la connexió.  
- **Consells bàsics:**  
  - No compartir dades sensibles.  
  - Mantenir la finestra oberta fins al final.  
  - Acceptar permisos quan es demanin.  

---

## 📚 Materials i links de suport
- **Moodle 0227 Serveis de Xarxa. UD4.AA3 Escriptoris Remots**

---

