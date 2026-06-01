# 🔐 T03: Seguretat Lògica - Recuperant Accés a Sistemes

## 📖 Breu descripció

Un client de la consultora EverPia ens ha facilitat una còpia virtual del disc dur d'un portàtil amb **Zorin OS**. El propietari de l'equip ha oblidat la contrasenya del seu compte i necessita recuperar l'accés a informació important emmagatzemada al sistema.

L'objectiu d'aquesta tasca és recuperar l'accés al sistema modificant la contrasenya de l'usuari existent i, posteriorment, investigar i implementar mesures de seguretat per evitar que aquest procediment pugui ser utilitzat per persones no autoritzades.

---

# 🎯 Objectius

* Crear una màquina virtual amb el disc proporcionat.
* Accedir al sistema mitjançant el menú GRUB.
* Identificar l'usuari existent.
* Restablir la contrasenya de l'usuari.
* Verificar que l'accés funciona correctament.
* Investigar mètodes de protecció del GRUB.
* Configurar una contrasenya al GRUB.
* Documentar tot el procediment.

---

# 🖥️ Creació de la màquina virtual

En primer lloc, es va crear una màquina virtual utilitzant VirtualBox i es va connectar el disc virtual proporcionat pel client.

### 📸 Captura de la configuració de la màquina virtual

![Configuració inicial de la màquina virtual](./img/vm-configuracio.png)

---

# 🔓 Recuperació de la contrasenya

## Accés al menú GRUB

Durant l'arrencada del sistema es va accedir al menú GRUB mantenint premuda la tecla **Shift**.

### 📸 Accés al menú GRUB

![Menú GRUB durant l'arrencada](./img/grub-menu.png)

---

## Mode Recovery

Des del menú GRUB es va seleccionar:

```bash
Advanced options for Zorin OS
```

Posteriorment:

```bash
Recovery Mode
```

I finalment:

```bash
root - Drop to root shell prompt
```

### 📸 Recovery Mode

![Accés al Recovery Mode](./img/recovery-mode.png)

---

# 👤 Identificació de l'usuari

Per identificar els usuaris existents es va executar la següent comanda:

```bash
ls /home
```

Resultat:

```bash
directiu
```

L'usuari identificat al sistema era:

**directiu**

### 📸 Identificació de l'usuari

![Identificació de l'usuari existent](./img/usuari.png)

---

# 🔑 Modificació de la contrasenya

Per canviar la contrasenya es va executar la comanda:

```bash
passwd directiu
```

A continuació es va introduir una nova contrasenya.

Exemple:

```bash
New password:
Retype new password:
passwd: password updated successfully
```

### 📸 Canvi de contrasenya

![Canvi de contrasenya de l'usuari](./img/passwd.png)

---

# ✅ Verificació de l'accés

Després de reiniciar el sistema:

```bash
reboot
```

Es va iniciar sessió amb l'usuari identificat i la nova contrasenya configurada.

L'accés es va realitzar correctament.

### 📸 Inici de sessió correcte

![Accés correcte al sistema](./img/login-correcte.png)

---

# 🛡️ Investigació: Com protegir el GRUB

Durant la investigació es va comprovar que qualsevol persona amb accés físic a l'equip podria modificar la contrasenya utilitzant el procediment anterior.

Per evitar-ho es recomana protegir el GRUB amb una contrasenya.

## Fonts consultades 📚

* https://waytoit.wordpress.com/2013/06/06/recuperando-password-en-ubuntu/
* https://help.ubuntu.com/community/Grub2/Passwords
* https://www.gnu.org/software/grub/manual/grub/grub.html

---

# 🔒 Configuració de contrasenya al GRUB

## Generació del hash de la contrasenya

Es va executar:

```bash
grub-mkpasswd-pbkdf2
```

Exemple de resultat:

```bash
PBKDF2 hash of your password is grub.pbkdf2.sha512...
```

### 📸 Generació del hash

![Generació del hash PBKDF2](./img/hash-grub.png)

---

## Modificació de la configuració

Es va editar el fitxer:

```bash
sudo nano /etc/grub.d/40_custom
```

Afegint:

```bash
set superusers="admin"
password_pbkdf2 admin grub.pbkdf2.sha512.10000...
```

### 📸 Configuració del GRUB

![Configuració del fitxer 40\_custom](./img/grub-config.png)

---

## Actualització del GRUB

Es va actualitzar la configuració executant:

```bash
sudo update-grub
```

Resultat:

```bash
Generating grub configuration file ...
Done
```

### 📸 Actualització del GRUB

![Actualització correcta del GRUB](./img/update-grub.png)

---

# 🧪 Verificació de la protecció

Després de reiniciar el sistema es va comprovar que per modificar les opcions d'arrencada o accedir a funcions avançades del GRUB és necessari introduir la contrasenya configurada.

### 📸 Verificació de la protecció

![GRUB protegit amb contrasenya](./img/grub-password.png)

---

# 📋 Conclusions

✅ S'ha recuperat l'accés al sistema modificant la contrasenya de l'usuari.

✅ S'ha identificat una vulnerabilitat relacionada amb l'accés físic a l'equip.

✅ S'ha investigat el funcionament del GRUB i les seves opcions de seguretat.

✅ S'ha implementat una contrasenya al GRUB per dificultar modificacions no autoritzades.

✅ El sistema és ara més segur davant intents de recuperació de contrasenyes per part de tercers.

---

# 🚀 Resultat final

El client ha recuperat l'accés a la informació del seu equip i s'han aplicat mesures addicionals de seguretat per protegir el sistema davant accessos físics no autoritzats.

