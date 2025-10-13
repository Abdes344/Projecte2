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





