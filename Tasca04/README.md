# 🐧 T04: Configurant i Administrant un Servidor Linux

## 📖 Breu descripció

Durant aquesta activitat s'ha configurat i administrat un servidor Linux amb l'objectiu de proporcionar serveis a una acadèmia de formació amb diverses seus.

La finalitat és centralitzar la gestió d'usuaris, grups i recursos de la xarxa, aplicant els coneixements adquirits al mòdul **0224 - Sistemes Operatius en Xarxa**.

---

# 🎯 Objectius

* Instal·lar i configurar un servidor Linux.
* Gestionar usuaris i grups.
* Configurar permisos i recursos compartits.
* Administrar serveis de xarxa.
* Verificar el correcte funcionament del servidor.
* Documentar tot el procediment realitzat.

---

# 🖥️ Preparació de l'entorn

Per realitzar la pràctica s'ha utilitzat una màquina virtual proporcionada pel tutor.

## Característiques de la màquina

| Component        | Valor                  |
| ---------------- | ---------------------- |
| Sistema Operatiu | Ubuntu Server / Debian |
| Memòria RAM      | 4 GB                   |
| CPU              | 2 nuclis               |
| Disc dur         | 20 GB                  |
| Xarxa            | Adaptador pont o NAT   |

### 📸 Configuració de la màquina virtual

![Configuració inicial de la màquina virtual](./img/vm-configuracio.png)

---

# ⚙️ Configuració inicial del servidor

Una vegada instal·lat el sistema operatiu es van actualitzar els paquets del sistema.

```bash
sudo apt update
sudo apt upgrade -y
```

### 📸 Actualització del sistema

![Actualització dels paquets](./img/update.png)

---

# 👥 Gestió d'usuaris i grups

## Creació de grups

Es van crear els grups necessaris per a l'organització.

```bash
sudo groupadd professors
sudo groupadd alumnes
sudo groupadd administradors
```

### 📸 Creació de grups

![Creació de grups](./img/grups.png)

---

## Creació d'usuaris

Es van crear diversos usuaris per a cada grup.

```bash
sudo useradd -m professor1
sudo passwd professor1
```

```bash
sudo useradd -m alumne1
sudo passwd alumne1
```

### 📸 Creació d'usuaris

![Creació d'usuaris](./img/usuaris.png)

---

## Assignació de grups

Els usuaris es van associar als grups corresponents.

```bash
sudo usermod -aG professors professor1
sudo usermod -aG alumnes alumne1
```

### 📸 Assignació de grups

![Assignació de grups als usuaris](./img/usermod.png)

---

# 📁 Gestió de directoris i permisos

Es van crear directoris compartits per als diferents departaments.

```bash
sudo mkdir /academia
sudo mkdir /academia/professors
sudo mkdir /academia/alumnes
```

Assignació de permisos:

```bash
sudo chown :professors /academia/professors
sudo chmod 770 /academia/professors
```

### 📸 Configuració de permisos

![Configuració de permisos](./img/permisos.png)

---

# 🌐 Configuració dels serveis

## Exemple: Servei SSH

Per permetre l'administració remota es va instal·lar SSH.

```bash
sudo apt install openssh-server -y
```

Comprovació del servei:

```bash
sudo systemctl status ssh
```

### 📸 Servei SSH en execució

![Servei SSH actiu](./img/ssh.png)

---

# 🔍 Verificacions

Es van realitzar diverses comprovacions per assegurar el correcte funcionament del servidor.

## Comprovació d'usuaris

```bash
cat /etc/passwd
```

## Comprovació de grups

```bash
cat /etc/group
```

## Comprovació de permisos

```bash
ls -la /academia
```

### 📸 Resultats de les verificacions

![Verificacions finals](./img/verificacions.png)

---

# 🛡️ Bones pràctiques de seguretat

Durant la configuració s'han aplicat diverses mesures de seguretat:

* 🔒 Utilització de contrasenyes segures.
* 👤 Principi de mínims privilegis.
* 📁 Assignació correcta de permisos.
* 🌐 Accés remot mitjançant SSH.
* 🔄 Actualització periòdica del sistema.
* 🛡️ Restricció d'accés als recursos sensibles.

---

# 📚 Recursos utilitzats

* Apunts UD3 - Sistemes Operatius en Xarxa.
* Documentació oficial d'Ubuntu.
* Documentació oficial de Debian.
* Manuals de Linux.

---

# ✅ Conclusions

Durant aquesta pràctica s'ha configurat correctament un servidor Linux destinat a la gestió d'una acadèmia de formació.

S'han creat usuaris, grups i directoris compartits, aplicant permisos adequats per garantir la seguretat del sistema.

A més, s'han configurat serveis bàsics d'administració i s'ha verificat el correcte funcionament de tots els components.

---

# 🚀 Resultat final

✔️ Servidor Linux instal·lat i configurat.

✔️ Usuaris i grups creats correctament.

✔️ Recursos compartits configurats.

✔️ Permisos aplicats segons les necessitats de l'organització.

✔️ Sistema preparat per donar servei a l'empresa client.

