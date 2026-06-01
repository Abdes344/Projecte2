# 🧑‍💻 T11: Instal·lació de WordPress en Local amb WP Local

## 📖 Breu descripció

En aquesta tasca s'ha creat una instal·lació de **WordPress en local** utilitzant l'eina **WP Local**.

Aquest entorn serveix com a espai de proves per aprendre el funcionament bàsic de WordPress, incloent la creació de pàgines, entrades, configuració del lloc i gestió de continguts.

Aquest lloc web serà utilitzat com a base per a pràctiques futures durant el curs.

---

# 🎯 Objectius

* Aprendre a utilitzar WP Local per crear un WordPress en local.
* Crear i configurar un lloc web de proves.
* Entendre l'estructura bàsica de WordPress.
* Diferenciar entre pàgines i entrades.
* Configurar el lloc web (pàgina inicial i blog).
* Crear contingut bàsic (pàgines i entrades).
* Mantenir un entorn de pràctiques estable durant el curs.

---

# ⚙️ Creació del lloc amb WP Local

## 🖥️ Pas 1: Crear el lloc

S'ha obert el programari **WP Local** i s'ha creat un nou lloc web.

### Dades utilitzades

* Nom del lloc: `web_proves_[Nom]`
* Usuari administrador: `[nom d’usuari]`
* Correu: `[correu de l’escola]`
* Contrasenya: (guardada per a ús personal)

### 📸 Creació del lloc

![Creació del lloc a WP Local](./img/wp-local-create.png)

---

## 🚀 Instal·lació completada

Un cop creat el lloc, WP Local ha generat automàticament:

* Servidor web local
* Base de dades MySQL
* Instal·lació de WordPress

---

# 🔑 Accés al tauler d’administració

L’accés al panell es fa mitjançant:

```text id="wpadmin"
http://web_proves_nom.local/wp-admin
```

Aquest espai és el **centre de control del lloc web**.

### 📸 Pantalla d’inici de sessió

![Login WordPress wp-admin](./img/wp-admin-login.png)

---

# 🧭 Diferència entre vista pública i administració

| Vista               | URL         | Descripció                        |
| ------------------- | ----------- | --------------------------------- |
| 🧑‍💻 Administrador | `/wp-admin` | Zona privada per gestionar el web |
| 👀 Pública          | `/`         | Web visible pels visitants        |

---

# 🎨 Canvi de tema

S'ha configurat el tema recomanat:

## Twenty Seventeen

### Motiu de selecció

* ✔️ Tema oficial de WordPress
* ✔️ Senzill i clar
* ✔️ Compatible amb editor clàssic i Gutenberg
* ✔️ Disseny responsive
* ✔️ Ideal per a aprenentatge

### 📸 Tema aplicat

![Tema Twenty Seventeen activat](./img/tema.png)

---

# 🧱 Creació de pàgines

## 🏠 Pàgina principal

**Títol:**

```
Benvinguts al meu web personal
```

### Contingut

Text de presentació personal utilitzant contingut dummy (Lorem Ipsum o text propi).

### 📸 Pàgina creada

![Pàgina d'inici creada](./img/pagina-inici.png)

---

## 🐾 Pàgina: Les meves mascotes

### Contingut

Descripció de mascotes reals o inventades.

També s'ha afegit una imatge mitjançant bloc d'imatge.

### 📸 Pàgina mascotes

![Pàgina de mascotes](./img/mascotes.png)

---

## 📬 Pàgina de contacte

### Títol

```
Contacte
```

### Contingut

Text d'invitació al contacte:

> Si vols contactar amb mi per parlar de sèries, tecnologia o gats, pots escriure’m.

### 📸 Pàgina contacte

![Pàgina de contacte](./img/contacte.png)

---

## 📰 Pàgina Blog

S'ha creat una pàgina anomenada:

```
Blog
```

Aquesta pàgina servirà com a contenidor d’entrades.

---

# ✍️ Creació d’entrades (Blog)

## 📌 Entrada 1

**Títol:**

```
Opinió sobre una sèrie - Capítol 1
```

Contingut generat amb ajuda de ChatGPT, incloent:

* Resum del capítol
* Opinió personal
* Imatges destacades
* Categories i etiquetes

### 📸 Entrada 1

![Entrada del blog capítol 1](./img/entrada1.png)

---

## 📌 Entrada 2

**Títol:**

```
Opinió sobre una sèrie - Capítol 2
```

### 📸 Entrada 2

![Entrada del blog capítol 2](./img/entrada2.png)

---

## 📌 Entrada 3

**Títol:**

```
Opinió sobre una sèrie - Capítol 3
```

### 📸 Entrada 3

![Entrada del blog capítol 3](./img/entrada3.png)

---

# 🆚 Diferència entre pàgines i entrades

| Pàgines 📄        | Entrades 📰        |
| ----------------- | ------------------ |
| Contingut estàtic | Contingut dinàmic  |
| No tenen data     | Ordenades per data |
| Estructura fixa   | Blog o notícies    |
| Exemple: Contacte | Exemple: Articles  |

---

# ⚙️ Configuració del lloc

## 🏠 Pàgina inicial estàtica

S'ha configurat:

* Pàgina d’inici: **Benvinguts al meu web personal**
* Pàgina de posts: **Blog**

Ruta:

```
Configuració → Lectura
```

### 📸 Configuració lectura

![Configuració de lectura WordPress](./img/lectura.png)

---

# 📚 Conclusions

Aquesta pràctica ha permès entendre el funcionament bàsic de WordPress en entorn local.

S'han creat pàgines, entrades i configuracions essencials per estructurar un lloc web complet.

També s'ha practicat la diferència entre contingut estàtic i dinàmic, fonamental per a qualsevol desenvolupament web.

---

# 🚀 Resultat Final

✔️ WordPress instal·lat en local amb WP Local.

✔️ Pàgines creades correctament.

✔️ Blog amb entrades funcionals.

✔️ Tema configurat.

✔️ Web preparada per a pràctiques futures.

