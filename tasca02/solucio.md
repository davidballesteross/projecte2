# ⚡ T02 – Selecció d’un SAI per una empresa client

**Autor:** David Ballesteros Antich  
**Curs:** 2B – CFGM Sistemes Microinformàtics i Xarxes  
**Mòdul:** Seguretat informàtica  
**Professora:** Isabel Bosch  
**Data:** 02/10/2025  
**Enllaç:** [Document original](https://docs.google.com/document/d/1R-FFYnsRPVyzYx2FpculMyQtKFhqpgO-tayO0LNToKQ/edit?usp=sharing)

---

## 📘 Índex
1. [Descripció del cas](#1-descripció-del-cas)  
2. [Càlculs de potència i reserva](#2-càlculs-de-potència-i-reserva)  
3. [Determinació de l’autonomia](#3-determinació-de-lautonomia)  
4. [Simulació i comparativa de models](#4-simulació-i-comparativa-de-models)  
5. [Solucions i justificació](#5-solucions-i-justificació)

---

## 1. Descripció del cas

L’empresa client és un petit despatx amb la següent infraestructura:

- 💻 4 ordinadors d’escriptori (400 W cadascun)  
- 🖥️ 4 monitors (30 W cadascun)  
- 🖨️ 1 impressora multifunció *(no es connectarà al SAI per l’alt consum i poc ús crític)*  
- 🌐 1 router d’accés a Internet  
- 🔌 Possibilitat d’afegir un switch per a la xarxa interna  

🎯 **Objectiu:** Seleccionar un **Sistema d’Alimentació Ininterrompuda (SAI)** que garanteixi la continuïtat del servei en cas de tall elèctric, amb autonomia suficient per fer un apagat segur i protegir la infraestructura crítica.

---

## 2. Càlculs de potència i reserva

Per determinar el SAI adequat, es calculen els consums reals dels equips:

| Equip | Quantitat | Consum (W) | Total (W) |
|--------|------------|-------------|------------|
| Ordinadors | 4 | 400 | 1600 |
| Monitors | 4 | 30 | 120 |
| Router | 1 | 20 | 20 |
| **Total** |  |  | **1.740 W** |

Com que no és recomanable que el SAI treballi sempre al límit, s’aplica una **reserva del 20%**:

Reserva = 1.740 W × 0,20 = 348 W
Potència total necessària = 1.740 W + 348 W = 2.088 W


Els fabricants de SAI indiquen la potència en **VA (Voltamperes)**.  
Per convertir W → VA es divideix pel factor de potència (aprox. 0,7):

2.088 W ÷ 0,7 ≈ 3.550 VA


> 🔋 El SAI ha de tenir **mínim 3.000 VA / 2.700 W** de potència.

---

## 3. Determinació de l’autonomia

L’autonomia mínima requerida és de **10 minuts**, suficient per:

- Continuar treballant en cas d’un tall breu.  
- Fer un **tancament segur dels sistemes** si el tall s’allarga.  

Amb una càrrega total de **2.088 W**, s’exclouen els models inferiors a 3 kVA.  
Per això, cal considerar SAI **professionals o amb bateries externes**, que garanteixin seguretat i marge suficient.

> 🔧 Es recomana un **SAI de 3 kVA**, que cobreix la potència amb reserva i manté un marge de seguretat adequat.

---

## 4. Simulació i comparativa de models

S’han analitzat dues opcions comercials de gamma professional.

### 🅰️ Opció A — APC Smart-UPS SRT 3000
- **Potència:** 3.000 VA / 2.700 W  
- **Tecnologia:** Online (doble conversió), sortida sinus pura  
- **Autonomia:**  
  - 3–4 min a plena càrrega  
  - 10+ min amb mòdul de bateries addicional *SRT96RMBP*  
- **Fiabilitat:** Alta, marca reconeguda a nivell empresarial  
- **Preu:** 3.200 € – 4.200 €

---

### 🅱️ Opció B — Eaton 9PX 3000
- **Potència:** 3.000 VA / 2.700 W (fins a 3.000 W en alguns models)  
- **Tecnologia:** Online (doble conversió)  
- **Autonomia:**  
  - 10–15 min a 2.100 W en models amb bateries de liti  
  - Possibilitat d’afegir *9PXEBM72RT* per ampliar autonomia  
- **Fiabilitat:** Excel·lent, amb eficiència energètica elevada  
- **Preu:** 3.200 € – 4.300 €

---

## 5. Solucions i justificació

Després de la comparativa, la millor opció és **Eaton 9PX 3000**.

### 🔎 Justificació:
1. ✅ Compleix amb l’autonomia mínima de 10 minuts **sense mòduls addicionals**.  
2. ⚙️ Permet **ampliar autonomia** si es connecten més equips en el futur.  
3. ♻️ Té **millor eficiència energètica**, reduint costos a llarg termini.  
4. 💰 Té un **preu similar a l’APC** però amb més prestacions d’origen.

---

### 🏁 Conclusió
El **Eaton 9PX 3000** és la solució més equilibrada entre **seguretat, escalabilitat i rendiment**.  
Garanteix la protecció de tots els sistemes del client davant possibles talls elèctrics, assegurant continuïtat operativa i tranquil·litat.

> 💡 *Un bon SAI no només protegeix els equips, sinó també la feina i la productivitat de tota l’empres
