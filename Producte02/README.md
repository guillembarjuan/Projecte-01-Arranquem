# P02 – Màquina virtual Ubuntu Server

## 📌 Descripció del producte

Aquest producte consisteix en una **màquina virtual (VM) amb Ubuntu Server** (versió LTS més recent) preparada per servir com a base per a la resta del curs. La màquina està configurada seguint uns requisits específics d’hardware virtual, xarxa i usuaris.

L’objectiu és disposar d’una **OVA (Open Virtual Appliance)** que permeti desplegar ràpidament un entorn de servidor Linux sense haver de repetir les configuracions inicials en cada pràctica.

A més, es va elaborar una **guia d’instal·lació** per documentar pas a pas tot el procés, seguint el lema del curs: *“Documentar, documentar i documentar”*.

---

## ⚙️ Requisits de la màquina virtual

| Paràmetre | Valor |
|-----------|-------|
| RAM | 4 GB |
| Disc dur | 20 GB |
| Adaptadors de xarxa | 2 |
| - Xarxa NAT | per accés a Internet |
| - Xarxa en pont | IP 192.168.2.x/24 (2n A) o 192.168.4.x/24 (2n B) |
| Usuari / contrasenya | `usuari` / `usuari` |
| Serveis addicionals | SSH instal·lat i actiu |

> *La IP concreta de l’adaptador en pont depèn del número de llista de cada alumne (x = número de llista).*

---

## 🛠️ Procés de creació

1. **Descàrrega de la ISO** d’Ubuntu Server (versió LTS).
2. **Creació de la VM** a VirtualBox (o VMware) amb els paràmetres de RAM, disc i 2 adaptadors de xarxa.
3. **Instal·lació del sistema operatiu**:
   - Configuració d’idioma, teclat, particionament per defecte.
   - Creació de l’usuari `usuari` amb contrasenya `usuari`.
   - Selecció del paquet `OpenSSH Server` durant la instal·lació.
4. **Configuració de xarxa posterior**:
   - L’adaptador NAT obté IP per DHCP.
   - L’adaptador en pont es configura amb IP estàtica `192.168.2.x` o `192.168.4.x`.
5. **Proves de connectivitat**:
   - `ping` a Internet (per NAT).
   - `ping` a l’amfitrió i a altres VMs de la mateixa xarxa en pont.
6. **Exportació a OVA** per tenir una plantilla reutilitzable.

---

## 📁 Contingut lliurat

- **Màquina virtual en format OVA** (emmagatzemada al repositori o enllaç extern).
- **Guia d’instal·lació** (document PDF o Markdown) amb:
  - Captures de pantalla de cada pas.
  - Explicació de les decisions preses.
  - Comprovació dels requisits.
  - Comandes bàsiques utilitzades.

---

## 💡 Aprenentatges

- Instal·lació bàsica d’Ubuntu Server en entorn virtualitzat.
- Configuració manual de xarxa amb Netplan (IP estàtica + NAT).
- Importància de documentar cada pas per facilitar futurs desplegaments.
- Exportació de màquines virtuals a OVA per reutilitzar-les.

---

## 👤 Autor

**Guillem Barjuan Alonso** – CFGM SMX  
Data de realització: primer trimestre del curs 2025-2026

---

*Aquest producte forma part del Projecte 01 – Arranquem i va ser la base per treballar amb servidors Linux durant la resta del curs.*
