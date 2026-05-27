# Pla de Recuperació davant Desastres (DRP)

## Introducció al cas

Recordeu el cas del portàtil al qual no es podia accedir?  

En aquella situació, la vostra perícia tant en la recuperació de l’accés com en la posterior fortificació del sistema va impressionar notablement el client. Per aquest motiu, ha decidit comptar novament amb vosaltres en aquest nou encàrrec.

El client ha encarregat l’elaboració d’un:

- **Pla de Contingència**
- **Pla de Continuïtat del Negoci**
- i especialment el **Pla de Recuperació davant Desastres (DRP — Disaster Recovery Plan)**

---

# Què és un DRP?

El Disaster Recovery Plan inclou:

- processos de restauració de dades,
- recuperació de hardware,
- restauració de software crític,
- i procediments per reprendre l’activitat normal tan ràpidament com sigui possible després d’un incident greu.

Exemples:
- robatori d’equips,
- avaries greus,
- corrupció de dades,
- ransomware,
- fallades de hardware,
- errors humans.

---

# Necessitat del client

Un dels punts crítics del DRP és garantir que els treballadors puguin disposar ràpidament dels seus equips de treball en cas d’incidència.

## ❌ Solució tradicional (NO viable)

No és acceptable:

- reinstal·lar el sistema operatiu manualment,
- aplicar configuracions una a una,
- reinstal·lar aplicacions,
- recuperar perfils manualment.

El temps de recuperació és crític per al negoci.

---

# Entorn tecnològic del client

## 💻 Sistemes operatius

Tota l’empresa treballa amb:

- **GNU/Linux**
- distribució:
  - **Zorin OS 18**

Els equips ja disposen de:
- configuracions específiques,
- aplicacions corporatives,
- entorns preparats per als usuaris.

---

# Fase 1 — Anàlisi i justificació de la solució tècnica

## Objectiu

Investigar eines capaces de:

- crear imatges completes del sistema,
- restaurar equips ràpidament,
- conservar:
  - configuracions,
  - aplicacions,
  - perfils,
  - dades.

---

# Comparativa d’eines

Cal elaborar una comparativa entre:

## 🏢 Solucions comercials
Trieu:
- 2 eines comercials

## 🌍 Solucions comunitàries / open source
Trieu:
- 2 eines de comunitat

---

# Aspectes a comparar

La comparativa ha d’incloure:

- característiques principals,
- compatibilitat amb Linux,
- restauració bare-metal,
- suport UEFI/GPT,
- compressió,
- clonació,
- restauració en xarxa,
- automatització,
- facilitat d’ús,
- suport tècnic,
- preu o model de llicència.

⚠️ Important:
La comparativa ha de ser:
- resumida,
- estructurada,
- analítica.

No ha de ser una còpia de les webs oficials.

---

# Proposta final

Després de la comparativa, haureu de:

## ✅ Escollir una solució

I justificar-la tenint en compte:

- cost,
- funcionalitats,
- facilitat de manteniment,
- escalabilitat,
- compatibilitat amb l’entorn Linux,
- rapidesa de recuperació.

---

# Fase 2 — Guia d’ús tècnica (Manual Operatiu)

## Objectiu de la prova de concepte

A partir de la màquina proporcionada pel client (OVA), caldrà:

### 1️⃣ Crear una imatge completa del sistema

Incloent:
- sistema operatiu,
- configuracions,
- aplicacions,
- dades.

---

### 2️⃣ Restaurar la imatge

Sobre una màquina virtual nova:

- mateixa RAM,
- mateix processador,
- mateixa mida de disc,
- mateixa configuració de xarxa,
- però sense sistema operatiu instal·lat.

---

# Documentació requerida

Cal elaborar una:

## 📘 Guia tècnica operativa

Pensada perquè el personal de manteniment pugui:

- crear còpies d’imatge,
- restaurar equips,
- repetir el procediment de forma segura.

---

# Requisits de la guia

La documentació ha de:

- explicar els passos detalladament,
- incorporar captures de pantalla rellevants,
- indicar possibles errors habituals,
- incloure verificacions finals,
- ser clara i replicable.

---

# Eina obligatòria per la prova de concepte

## 🛠️ Rescuezilla

Tot i que la proposta final podria ser una altra eina, la guia tècnica d’aquesta pràctica s’ha de realitzar utilitzant:

- **Rescuezilla**

---

# Tipus de tasca

## 👤 Tasca individual

---

# Materials i recursos de suport

## 🌐 INCIBE
**¿Ya tienes tu Plan de Recuperación ante Desastres?**

https://www.incibe.es/empresas/blog/tienes-tu-plan-recuperacion-desastres

---

## 🌐 Web oficial de Rescuezilla

https://rescuezilla.com/
