# Projecte2 - Afegint la Documentació de Seguretat al Repositori

## Breu descripció

Al llarg d'aquest projecte s'han elaborat diverses guies tècniques relacionades amb la seguretat informàtica. Per evitar que aquesta informació quedi dispersa en diferents documents (*data silo*), s'utilitzarà Git i GitHub per centralitzar tota la documentació en un únic repositori amb control de versions.

L'objectiu és disposar d'un espai organitzat, accessible i fàcil de mantenir, on es pugui consultar tota la documentació generada durant el projecte.

---

# Objectius

* Crear un repositori anomenat **Projecte2**.
* Utilitzar **Markdown** per documentar totes les activitats.
* Organitzar la documentació en carpetes segons les tasques realitzades.
* Incloure captures de pantalla amb descripcions alternatives.
* Facilitar la navegació entre documents mitjançant hipervincles.

---

# Estructura del Repositori

```text
Projecte2/
│
├── README.md
│
├── Tasca2/
│   ├── README.md
│   ├── solucio.md
│   └── img/
│       ├── captura1.png
│       └── captura2.png
│
├── Tasca3/
│   ├── README.md
│   ├── solucio.md
│   └── img/
│       ├── captura1.png
│       └── captura2.png
```

---

# Contingut del Projecte

## Tasca 2

La carpeta **Tasca2** conté tota la documentació relacionada amb la segona activitat del projecte.

### Arxius inclosos

* `README.md`
* `solucio.md`
* Carpeta `img/` amb les captures de pantalla

### Accés directe

[Veure la solució de la Tasca 2](./Tasca2/solucio.md)

---

## Tasca 3

La carpeta **Tasca3** conté tota la documentació relacionada amb la tercera activitat del projecte.

### Arxius inclosos

* `README.md`
* `solucio.md`
* Carpeta `img/` amb les captures de pantalla

### Accés directe

[Veure la solució de la Tasca 3](./Tasca3/solucio.md)

---

# Exemple de README per a cada Tasca

## README de Tasca2

```markdown
# Tasca 2

## Descripció

Aquesta carpeta conté la documentació corresponent a la Tasca 2.

## Contingut

- solucio.md
- Carpeta img amb les captures de pantalla

## Accés ràpid

[Veure la solució](./solucio.md)
```

## README de Tasca3

```markdown
# Tasca 3

## Descripció

Aquesta carpeta conté la documentació corresponent a la Tasca 3.

## Contingut

- solucio.md
- Carpeta img amb les captures de pantalla

## Accés ràpid

[Veure la solució](./solucio.md)
```

---

# Exemple de Documentació (solucio.md)

```markdown
# Solució de la Tasca

## Objectiu

Descriure el procediment seguit per completar la tasca.

## Pas 1: Preparació

Explicació del primer pas realitzat.

![Captura de pantalla del primer pas](./img/captura1.png)

## Pas 2: Configuració

Explicació de la configuració efectuada.

![Captura de pantalla de la configuració realitzada](./img/captura2.png)

## Resultat

La tasca s'ha completat correctament.

## Conclusions

Resum dels coneixements adquirits i dels objectius assolits.
```

---

# Imatges i Accessibilitat

Totes les captures de pantalla s'han de guardar en format **PNG** dins de la carpeta `img` corresponent a cada tasca.

Cada imatge ha d'incloure una descripció alternativa (*alt text*) per garantir l'accessibilitat.

### Exemple correcte

```markdown
![Captura de pantalla de la configuració del tallafoc](./img/firewall.png)
```

### Exemple incorrecte

```markdown
![](./img/firewall.png)
```

---

# Tecnologies Utilitzades

* Git
* GitHub
* Markdown

---

# Lliurable

## Repositori GitHub

Enllaç al repositori:

```text
https://github.com/usuari/Projecte2
```

El repositori ha de contenir:

* README principal del projecte.
* Carpeta Tasca2 amb README, solució i imatges.
* Carpeta Tasca3 amb README, solució i imatges.
* Tota la documentació en format Markdown.
* Captures de pantalla amb text alternatiu descriptiu.

