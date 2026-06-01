# 🌐 T06: El Servei de DHCP - Configuració Pràctica

## 📖 Breu descripció

En aquesta pràctica s'ha configurat un servidor **DHCP** sobre **Ubuntu Server** amb l'objectiu d'automatitzar l'assignació d'adreces IP dins de la xarxa local de l'empresa client.

El servidor DHCP permet assignar automàticament adreces IP, porta d'enllaç i servidors DNS als equips clients, evitant errors de configuració manual i millorant la gestió de la infraestructura de xarxa.

---

# 🎯 Objectius

* Instal·lar i configurar un servidor DHCP.
* Definir un rang d'adreces IP dinàmiques.
* Configurar la porta d'enllaç i el servidor DNS.
* Verificar el funcionament del servei.
* Capturar la negociació DHCP amb Wireshark.
* Configurar una reserva DHCP per a un client específic.
* Documentar tot el procés.

---

# 🖥️ Entorn de treball

## Servidor

| Paràmetre        | Valor           |
| ---------------- | --------------- |
| Sistema Operatiu | Ubuntu Server   |
| Servei           | ISC DHCP Server |
| Xarxa            | 192.169.X.0/24  |

## Client

| Paràmetre        | Valor    |
| ---------------- | -------- |
| Sistema Operatiu | Zorin OS |
| Configuració IP  | DHCP     |

> **Nota:** Substituir **X** pel vostre número de llista.

---

# ⚙️ Instal·lació del Servidor DHCP

Actualitzem els paquets del sistema:

```bash
sudo apt update
sudo apt upgrade -y
```

Instal·lem el servei DHCP:

```bash
sudo apt install isc-dhcp-server -y
```

### 📸 Instal·lació del servei

![Instal·lació del paquet isc-dhcp-server](./img/installacio-dhcp.png)

---

# 🔧 Configuració de la interfície de xarxa

Comprovem el nom de la interfície:

```bash
ip a
```

Exemple:

```bash
ens33
```

Editem el fitxer:

```bash
sudo nano /etc/default/isc-dhcp-server
```

Configuració:

```bash
INTERFACESv4="ens33"
```

### 📸 Configuració de la interfície

![Configuració de la interfície DHCP](./img/interficie.png)

---

# 📝 Configuració del fitxer DHCP

Editem el fitxer principal:

```bash
sudo nano /etc/dhcp/dhcpd.conf
```

Configuració:

```bash
authoritative;

subnet 192.169.X.0 netmask 255.255.255.0 {

    range 192.169.X.100 192.169.X.200;

    option routers 192.169.X.254;

    option domain-name-servers 8.8.8.8;

    default-lease-time 600;

    max-lease-time 7200;
}
```

### 📸 Configuració del fitxer dhcpd.conf

![Configuració del servidor DHCP](./img/dhcpd-conf.png)

---

# 🔄 Reinici del Servei

Reiniciem el servei:

```bash
sudo systemctl restart isc-dhcp-server
```

Comprovem l'estat:

```bash
sudo systemctl status isc-dhcp-server
```

Verificació:

```bash
active (running)
```

### 📸 Servei funcionant

![Servei DHCP en execució](./img/status-dhcp.png)

---

# 🔍 Verificació de la Configuració

Comprovem la sintaxi del fitxer:

```bash
sudo dhcpd -t
```

Resultat:

```bash
Syntax: OK
```

### 📸 Verificació de la sintaxi

![Verificació correcta de la configuració](./img/test-config.png)

---

# 💻 Configuració del Client Zorin

A la màquina client es configura la xarxa perquè obtingui la IP automàticament.

### 📸 Configuració DHCP del client

![Configuració automàtica de xarxa](./img/client-dhcp.png)

---

# 📡 Obtenció d'Adreça IP

Al client es renova la configuració:

```bash
sudo dhclient -r
sudo dhclient
```

Comprovem la IP assignada:

```bash
ip a
```

Resultat:

```bash
192.169.X.101
```

### 📸 IP assignada pel servidor

![IP rebuda del servidor DHCP](./img/ip-client.png)

---

# 🌍 Verificació de Gateway i DNS

Comprovació de la porta d'enllaç:

```bash
ip route
```

Resultat:

```bash
default via 192.169.X.254
```

Comprovació del DNS:

```bash
cat /etc/resolv.conf
```

Resultat:

```bash
nameserver 8.8.8.8
```

### 📸 Gateway i DNS

![Comprovació del Gateway i DNS](./img/gateway-dns.png)

---

# 📊 Captura de la Negociació DHCP

S'ha utilitzat Wireshark per capturar el procés DORA:

## Discover

```text
DHCP Discover
```

## Offer

```text
DHCP Offer
```

## Request

```text
DHCP Request
```

## Acknowledge

```text
DHCP ACK
```

### 📸 Captura de Wireshark

![Negociació DHCP completa](./img/wireshark-dora.png)

---

# 📌 Configuració d'una Reserva DHCP

Obtenim l'adreça MAC del client:

```bash
ip link
```

Exemple:

```bash
08:00:27:12:34:56
```

Afegim al fitxer `dhcpd.conf`:

```bash
host zorin-client {

    hardware ethernet 08:00:27:12:34:56;

    fixed-address 192.169.X.80;
}
```

### 📸 Configuració de la reserva

![Reserva DHCP configurada](./img/reserva-dhcp.png)

---

# 🔄 Aplicació de la Reserva

Reiniciem el servei:

```bash
sudo systemctl restart isc-dhcp-server
```

Al client:

```bash
sudo dhclient -r
sudo dhclient
```

Comprovem la nova IP:

```bash
ip a
```

Resultat:

```bash
192.169.X.80
```

### 📸 Adreça reservada assignada

![IP fixa assignada per reserva](./img/ip-reservada.png)

---

# 🛡️ Bones Pràctiques

* Utilitzar rangs DHCP ben definits.
* Reservar IPs per a servidors i impressores.
* Supervisar les concessions actives.
* Fer còpies de seguretat de la configuració.
* Mantenir el sistema actualitzat.
* Restringir l'accés administratiu al servidor.

---

# 📚 Recursos Utilitzats

* Apunts UD2 Configuració Servidor DHCP.
* Moodle - Serveis de Xarxa.
* Documentació oficial d'Ubuntu.
* Manual d'ISC DHCP Server.

---

# ✅ Conclusions

Durant aquesta pràctica s'ha desplegat correctament un servidor DHCP sobre Ubuntu Server.

S'ha configurat un rang d'adreces IP dinàmiques, la porta d'enllaç i el servidor DNS, verificant que els clients obtenen automàticament la configuració de xarxa.

També s'ha capturat la negociació DHCP mitjançant Wireshark i s'ha implementat una reserva DHCP basada en l'adreça MAC del client.

---

# 🚀 Resultat Final

✔️ Servidor DHCP instal·lat.

✔️ Configuració validada sense errors.

✔️ Assignació automàtica d'IPs funcional.

✔️ Gateway i DNS distribuïts correctament.

✔️ Negociació DORA capturada amb Wireshark.

✔️ Reserva DHCP configurada i verificada correctament.

