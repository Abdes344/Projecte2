# 📝 Estudi i tria d’un SAI per a TecnoGestió S.L.

## 📌 Objectiu
Realitzar un estudi tècnic per seleccionar un **SAI (Sistema d’Alimentació Ininterrompuda)** adequat per a l’oficina de l’empresa TecnoGestió S.L., tenint en compte les seves necessitats energètiques i la protecció dels equips informàtics davant talls de subministrament elèctric.

---

## ✅ Tasques a realitzar

### 1. Inventari d’equips
- Elaborar una **llista detallada** dels dispositius que es connectaran al SAI:
  - Ordinadors
  - Monitors
  - Impressora multifunció
  - Router
- **Justificar** si algun dispositiu **no** s’ha de connectar al SAI (per exemple, equips amb alt consum que no requereixen mantenir-se actius durant un tall de llum).

---

### 2. Consulta d’especificacions tècniques
- Cercar les **dades de consum elèctric** de cada dispositiu.
- Triar models de dispositius **similars als que podria tenir l’empresa**.
- Indicar clarament:
  - Model triat
  - Consum en **Watts (W)** i en **VA (Volt-Amperes)**

---

### 3. Càlcul de potència total
- **Sumar** el consum total de tots els dispositius que es connectaran al SAI.
- Afegir un **marge de seguretat del 20%** sobre la potència total calculada.

---

### 4. Determinació de l’autonomia necessària
- Estimar el **temps mínim** durant el qual el SAI hauria de mantenir els equips en funcionament (exemple: **10 minuts** per poder desar documents i apagar els equips de manera segura).

---

### 5. Recerca de models de SAI
- Buscar **2 o 3 models comercials** de SAI que compleixin els requisits calculats (potència i autonomia).
- Comparar els models en base a:
  - Potència (W i VA)
  - Temps d’autonomia
  - Nombre i tipus de sortides
  - Preu
  - Marca i qualitat

---

### 6. Informe tècnic
- Redactar un **informe tècnic** estructurat amb els següents punts:
  - Càlculs de potència i autonomia
  - Models de SAI analitzats
  - Comparativa de característiques
  - **Justificació de la tria final**
- Incloure **material de suport** com enllaços a pàgines dels productes, fulls tècnics, imatges, etc.

---

## 📂 Format de lliurament
L’informe ha d’estar redactat amb claredat i ben estructurat. Es pot lliurar en format **Markdown**, PDF o Word, segons s’indiqui per part del responsable del projecte.

---


## SOLUCIÓ 💡

# Informe Tècnic: Estudi i Tria d’un SAI per a TecnoGestió S.L.

## Inventari d’equips

| Tipus d’equip                                 | Quantitat | Model                                            | Watts per unitat | VA per unitat |
|----------------------------------------------|-----------|--------------------------------------------------|------------------|---------------|
| Ordinador de sobretaula + Monitor            | 4         | ThinkCentre M70a Gen 6 (24") + Monitor 90W       | 180 W            | 202 VA        |
| Router                                        | 1         | Starlink Mini Kit WiFi IP67                      | 40 W             | 57 VA         |
| Impressora-fotocopiadora multifunció         | 1         | (No connectada al SAI - veure justificació)      | -                | -             |

> **Justificació:** No es connecta la impressora-fotocopiadora multifunció al SAI ja que el seu consum energètic és molt elevat i no és essencial durant una caiguda de subministrament. La seva connexió podria reduir considerablement l'autonomia del sistema d’alimentació ininterrompuda.

---

## Càlcul de potència total

| Equip                     | Quantitat | Watts totals | VA totals |
|--------------------------|-----------|--------------|-----------|
| Ordinador + Monitor      | 4         | 360 W        | 404 VA    |
| Router                   | 1         | 40 W         | 57 VA     |
| **Total sense reserva**  | -         | **400 W**    | **461 VA**|

### Aplicació de reserva del 20%:

- **Watts amb reserva:** `400 W x 1,20 = 480 W`
- **VA amb reserva:** `461 VA x 1,20 = 553 VA`

---

## Determinació de l’autonomia necessària

- **Objectiu:** Garantir mínim **10 minuts** per tancar els equips de forma segura.
- **Consum estimat:** 480 W

### Exemple de càlcul amb model Salicru:

- **Bateria:** 12 V / 9 Ah = 108 Wh
- **Autonomia:** `108 Wh / 480 W = 0,225 h = 13,5 minuts`

> **Resultat:** Autonomia suficient per tancar equips de forma segura.

---

## Recerca de models de SAI

| Característica              | Salicru SPS SOHO+ 2200VA | APC Easy UPS BVX2200LI-GR | Riello NPW-1000 600W      |
|----------------------------|---------------------------|----------------------------|---------------------------|
| **Potència**               | 2200 VA / 1200 W          | 2200 VA / 1200 W           | 1000 VA / 600 W           |
| **Autonomia estimada**     | 11-12 minuts              | 11-12 minuts               | 8-10 minuts               |
| **Tipus de sortides**      | 4 Schuko + 2 USB          | 4 Schuko                   | 6 IEC                     |
| **Preu aproximat**         | 235,99 €                  | 239 €                      | 139 €                     |
| **Marca**                  | Salicru                   | APC                        | Riello                    |

---

## Informe tècnic

### Models analitzats

1. **Salicru SPS SOHO+ 2200VA**
2. **APC Easy UPS BVX2200LI-GR**
3. **Riello NPW-1000 600W**

### Justificació de la selecció final

> Es recomana el **Salicru SPS SOHO+ 2200VA**, ja que ofereix:
> - Una **potència adequada** per suportar els equips necessaris amb reserva.
> - **Autonomia suficient** per garantir el tancament segur dels dispositius.
> - **Més funcionalitats** com ports USB addicionals.
> - Una **bona relació qualitat-preu**.
> 
> És una opció fiable i de fàcil integració en l'entorn de TecnoGestió S.L.

---




