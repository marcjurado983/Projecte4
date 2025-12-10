# 🗂️ Servidor de fitxers Linux amb NFS

Aquesta guia documenta pas a pas la configuració d’un servidor NFS a Ubuntu Server i la connexió des d’un client Linux (Zorin OS). Inclou explicacions, comandes i captures numerades.

---

## 1. Creació de grups i usuaris

Primer definim els grups de treball i els usuaris que hi pertanyen:

```bash
sudo groupadd devs
sudo groupadd admins
sudo useradd -m -s /bin/bash -G devs dev01
sudo useradd -m -s /bin/bash -G admins admin01
sudo passwd dev01
sudo passwd admin01


## 1. Creació de grups i usuaris
