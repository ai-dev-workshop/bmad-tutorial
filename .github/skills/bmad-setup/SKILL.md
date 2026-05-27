---
name: bmad-setup
description: "Install and set up the BMAD Method in this project. Use when: installing bmad, setting up bmad-method, getting started with bmad, initializing bmad, first time bmad setup, telepíteni a bmad-ot, bmad telepítés, projekt beállítás."
argument-hint: "Optional: specify modules (e.g. bmad-method, enterprise) or track (quick-flow, bmad-method, enterprise)"
---

# BMAD Method – Telepítési és Beállítási Útmutató

Segít telepíteni és konfigurálni a [BMAD Method](https://docs.bmad-method.org/tutorials/getting-started/) keretrendszert ebbe a projektbe, majd eligazít a következő lépések között.

## Mikor Használd

- BMAD Method első telepítésekor egy projektbe
- Modulok hozzáadásakor vagy eltávolításakor meglévő telepítésből
- Ha nem tudod, merre indulj el a BMAD-dal

---

## Előfeltételek Ellenőrzése

Mielőtt elindítod a telepítést, ellenőrizd a következőket:

1. **Node.js 20.12+** — A telepítőhöz szükséges  
   ```bash
   node --version
   ```
2. **Git** — Külső modulok klónozásához ajánlott  
   ```bash
   git --version
   ```
3. **AI IDE** — Claude Code, Cursor vagy hasonló eszköz legyen nyitva a projektmappában

Ha valamelyik hiányzik, telepítsd fel a folytatás előtt.

---

## Telepítési Eljárás

### 1. lépés – Installer futtatása

Nyiss egy terminált a **projektmappában**, majd futtasd:

```bash
npx bmad-method install
```

> Ha a legújabb előzetes verziót szeretnéd (nem kötelező):
> ```bash
> npx bmad-method@next install
> ```

### 2. lépés – Interaktív telepítési kérdések megválaszolása

A telepítő 5 kérdést tesz fel. Javasolt válaszok:

| Kérdés | Javasolt válasz |
|--------|-----------------|
| Telepítési könyvtár | Fogadd el az alapértelmezett értéket (aktuális mappa) |
| Modulok kiválasztása | Válaszd a **BMad Method**-ot (alap választás legtöbb projekthez) |
| Kész a telepítésre? | **Igen** — a legújabb stabil verzió lesz telepítve |
| AI eszközök / IDE integráció | Válaszd a te IDE-det (pl. claude-code, cursor) |
| Modulonkénti konfiguráció | Projekt neve, programnyelv, kimeneti mappa |

**Melyik modult válaszd?**

| Track | Mikor válaszd | Telepítendő modul |
|-------|---------------|-------------------|
| **Quick Flow** | Hibajavítás, kis funkció (1–15 story) | BMad Method |
| **BMad Method** | Termékek, platformok, összetett funkciók (10–50+ story) | BMad Method |
| **Enterprise** | Compliance, multi-tenant rendszerek (30+ story) | Enterprise |

### 3. lépés – Telepítés ellenőrzése

A telepítés után két mappa jön létre:

```
_bmad/          ← agents, workflows, tasks, konfiguráció
_bmad-output/   ← üres; itt lesznek az artefaktok
```

Ellenőrizd, hogy mindkét mappa létrejött-e.

---

## Telepítés Utáni Első Lépés

Az AI IDE-ben (új chatablakban) futtasd:

```
bmad-help
```

A **BMad-Help** agent:
- Megvizsgálja a projekt jelenlegi állapotát
- Megmutatja az elérhető lehetőségeket
- Megmondja, mi a következő kötelező lépés

Kérdezhetsz is tőle, például:
```
bmad-help van egy SaaS ötletem, hol kezdjem?
bmad-help milyen lehetőségeim vannak?
```

---

## A Fejlesztési Folyamat Áttekintése

A BMAD 4 fázisból áll:

```
Fázis 1: Analízis    → brainstorming, kutatás, product brief (opcionális)
Fázis 2: Tervezés    → PRD / spec létrehozása (kötelező)
Fázis 3: Megoldás    → architektúra tervezés (BMad Method / Enterprise)
Fázis 4: Megvalósítás → epic-enként, story-nként implementáció
```

**Fontos:** Minden workflow-hoz indíts **új chat ablakot** az AI IDE-ben.

---

## Meglévő Telepítés Frissítése

Ha `_bmad/` már létezik, a `npx bmad-method install` egy menüt ad:

- **Quick Update** — meglévő beállításokkal frissít, gyors, nem-interaktív
- **Modify Install** — teljes interaktív folyamat, modulok hozzáadása/eltávolítása

---

## Hivatkozások

- [Getting Started Tutorial](https://docs.bmad-method.org/tutorials/getting-started/)
- [How to Install BMad](https://docs.bmad-method.org/how-to/install-bmad/)
- [Workflow Map](https://docs.bmad-method.org/reference/workflow-map/)
- [BMAD GitHub](https://github.com/bmad-code-org/BMAD-METHOD)
