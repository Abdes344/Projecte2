# 🌐 T05: El Servei DHCP - Introducció Teòrica

## 📖 Breu descripció

En aquesta activitat s'ha realitzat una introducció teòrica al funcionament del servei **DHCP (Dynamic Host Configuration Protocol)**.

L'objectiu és comprendre com funciona aquest protocol, quina és la seva utilitat dins d'una xarxa informàtica i quins avantatges aporta respecte a la configuració manual de les adreces IP.

Aquesta formació és necessària abans de poder desplegar i administrar un servidor DHCP en un entorn real.

---

# 🎯 Objectius

* Comprendre què és el protocol DHCP.
* Entendre el funcionament de l'assignació automàtica d'adreces IP.
* Conèixer els components implicats en el procés.
* Identificar els avantatges i inconvenients del servei.
* Preparar-se per a la configuració pràctica d'un servidor DHCP.

---

# 🤔 Què és DHCP?

**DHCP (Dynamic Host Configuration Protocol)** és un protocol de xarxa que permet assignar automàticament configuracions de xarxa als dispositius connectats.

Gràcies a DHCP, un equip pot obtenir automàticament:

* 📍 Adreça IP
* 🌐 Màscara de subxarxa
* 🚪 Porta d'enllaç predeterminada (Gateway)
* 🔎 Servidors DNS
* ⏱️ Temps de concessió de la IP

Sense DHCP, tota aquesta informació hauria de configurar-se manualment a cada dispositiu.

---

# 🏗️ Components del Servei DHCP

## 🖥️ Servidor DHCP

És l'equip encarregat d'assignar les configuracions de xarxa als clients.

Les seves funcions principals són:

* Gestionar les adreces IP disponibles.
* Assignar IPs als clients.
* Renovar concessions.
* Evitar adreces duplicades.

---

## 💻 Client DHCP

És qualsevol dispositiu que sol·licita una configuració de xarxa automàtica.

Exemples:

* Ordinadors
* Portàtils
* Telèfons mòbils
* Impressores
* Tablets

---

# 🔄 Funcionament del Protocol DHCP

El procés DHCP es basa en quatre fases principals conegudes com:

## DORA

### 1️⃣ Discover

El client envia un missatge de difusió (*broadcast*) buscant servidors DHCP.

```text id="4e9yfe"
DHCP Discover
```

---

### 2️⃣ Offer

El servidor respon oferint una adreça IP disponible.

```text id="szn0kj"
DHCP Offer
```

---

### 3️⃣ Request

El client accepta l'oferta i sol·licita formalment aquella IP.

```text id="jv2d7g"
DHCP Request
```

---

### 4️⃣ Acknowledge

El servidor confirma l'assignació.

```text id="j4m8r6"
DHCP Acknowledge
```

---

# 📊 Esquema del Procés DORA

```text id="r0s3pp"
Client                         Servidor DHCP
  |                                   |
  |------ DHCP Discover ------------->|
  |                                   |
  |<------- DHCP Offer ---------------|
  |                                   |
  |------ DHCP Request -------------->|
  |                                   |
  |<----- DHCP Acknowledge -----------|
  |                                   |
```

---

# 📍 Què és una Concessió (Lease)?

Una concessió és el temps durant el qual una adreça IP està reservada per a un dispositiu.

Exemple:

```text id="m0gvg4"
Lease Time = 24 hores
```

Durant aquest període la IP queda associada al client.

Quan el temps expira:

* El client intenta renovar-la.
* El servidor pot mantenir-la o assignar-ne una de nova.

---

# ✅ Avantatges del DHCP

### 🚀 Automatització

No cal configurar manualment cada dispositiu.

### ⚡ Rapidesa

Els equips es connecten a la xarxa de forma immediata.

### 🛡️ Menys errors

Evita errors humans en la configuració d'IPs.

### 📈 Escalabilitat

Permet gestionar grans quantitats de dispositius.

### 🔄 Gestió centralitzada

Tota la configuració es controla des d'un únic servidor.

---

# ❌ Inconvenients del DHCP

### 🔌 Dependència del servidor

Si el servidor DHCP falla, els nous equips no podran obtenir configuració.

### ⚠️ Risc de servidors DHCP no autoritzats

Un atacant podria desplegar un servidor DHCP fraudulent.

### 🛡️ Necessitat de seguretat

Cal protegir adequadament el servei per evitar manipulacions.

---

# 🌍 Exemple d'Assignació DHCP

Suposem una xarxa:

```text id="b5xbgr"
Xarxa: 192.168.1.0/24
```

Configuració del servidor:

| Paràmetre  | Valor                         |
| ---------- | ----------------------------- |
| Rang DHCP  | 192.168.1.100 - 192.168.1.200 |
| Gateway    | 192.168.1.1                   |
| DNS        | 8.8.8.8                       |
| Lease Time | 24 hores                      |

Quan un ordinador es connecta, podria rebre:

```text id="7y60bg"
IP: 192.168.1.105
Màscara: 255.255.255.0
Gateway: 192.168.1.1
DNS: 8.8.8.8
```

---

# 🔒 Bones Pràctiques de Seguretat

* Utilitzar rangs d'adreces adequats.
* Controlar els dispositius connectats.
* Supervisar les concessions actives.
* Evitar servidors DHCP no autoritzats.
* Fer còpies de seguretat de la configuració.
* Mantenir el servidor actualitzat.

---

# 📚 Recursos Utilitzats

* Apunts UD2 - El Servei DHCP.
* Moodle del mòdul 0227 Serveis de Xarxa.
* Documentació oficial de Linux.
* Documentació de l'Internet Engineering Task Force (IETF).

---

# 📝 Conclusions

El protocol DHCP és una peça fonamental en qualsevol xarxa moderna, ja que permet automatitzar la configuració dels dispositius i simplifica enormement la seva administració.

Comprendre el seu funcionament és imprescindible abans de desplegar un servidor DHCP real, ja que permet gestionar correctament les adreces IP i mantenir una infraestructura de xarxa eficient i segura.

---

# 🚀 Resultat Final

✔️ Comprensió del protocol DHCP.

✔️ Coneixement del procés DORA.

✔️ Identificació dels components implicats.

✔️ Preparació per a la configuració pràctica d'un servidor DHCP en Linux.

