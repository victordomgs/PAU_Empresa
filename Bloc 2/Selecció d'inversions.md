<h1 align="center">Selecció d'inversions
<div align="center">

## Continguts

- [1. Selecció millor inversió](#1-selecció-millor-inversió)

## 1. Selecció millor inversió

La **inversió** és l'activitat que l'empresa porta a terme en el present per comprar béns i obtenir beneficis en el futur.

### Característiques financeres d'una inversió

| Element | Símbol | Definició |
|---|---|---|
| Desemborsament inicial | $D_0$ | Quantitat de diners que es destinen a la inversió en el moment zero (signe negatiu, és una sortida de diners) |
| Durada temporal | $n$ | Nombre d'anys que dura la inversió |
| Fluxos nets de caixa | $F_i$ | Diferència entre els cobraments ($C_i$) i els pagaments ($P_i$) de cada any: $F_i = C_i - P_i$ |
| Valor residual | $R$ | Valor del bé al final de la seva vida útil. S'afegeix a l'últim flux de caixa |

> [!IMPORTANT]
> Els **fluxos nets de caixa** (cobraments − pagaments) **no** són el mateix que els ingressos − despeses.

### Representació gràfica

```
−D₀      F₁      F₂  ...      Fₙ = Cₙ + R − Pₙ
 |--------|--------|------------|
 0        1        2            n
```

---

### Tipus de Mètodes de Selecció

Abans de triar una inversió, cal comparar les alternatives disponibles. Hi ha dos grans tipus de mètodes:

| | Mètodes Estàtics | Mètodes Dinàmics |
|---|---|---|
| **Factor temps** | No el tenen en compte | Sí el tenen en compte |
| **Supòsit** | El valor dels diners és constant en el temps | El valor dels diners varia segons el moment |
| **Exemple** | Pay-back | VAN, TIR |

### Mètode Estàtic: Pay-back (Termini de Recuperació)

#### Definició

El **pay-back** calcula el **temps que tardarà l'empresa a recuperar el desemborsament inicial** de la inversió. Si s'ha de triar entre diverses inversions, s'escull la que permet recuperar abans el capital invertit.

> [!NOTE]
> El pay-back **no té en compte** el valor dels diners en el temps, ni el volum total dels fluxos de caixa ni la magnitud del desemborsament inicial.

#### Càlcul

**Cas 1 — Fluxos anuals iguals:**

$$\text{Pay-back} = \frac{D_0}{F_i}$$

**Cas 2 — Fluxos anuals desiguals:**

S'acumulen els fluxos any a any fins arribar al desemborsament inicial. Si la recuperació es produeix entre dos períodes, es calcula la fracció de temps, assumint que el flux es recupera de manera constant al llarg de l'any.

#### Criteri de decisió

- Si s'ha de triar entre diverses inversions → **s'escull la que tingui el pay-back més petit** (es recupera abans).
- Un pay-back més petit implica menys risc.

#### Exemple amb flux de caixa desigual

| Any | Flux de caixa ($F_i$) | Acumulat |
|---|---|---|
| 0 | −10.000 € | −10.000 € |
| 1 | 3.000 € | −7.000 € |
| 2 | 4.000 € | −3.000 € |
| 3 | 5.000 € | +2.000 € |

La recuperació es produeix entre l'any 2 i l'any 3. Com que al final de l'any 2 falten 3.000 € i el flux de l'any 3 és 5.000 €:

$$\text{Fracció} = \frac{3.000}{5.000} = 0{,}6 \text{ anys}$$

$$\text{Pay-back} = 2 + 0{,}6 = \textbf{2,6 anys}$$

### Mètodes Dinàmics

Els mètodes dinàmics **sí que tenen en compte el moment en el temps** en què es produeixen els fluxos de caixa. Utilitzen la capitalització i el descompte per homogeneïtzar els fluxos.

### VAN — Valor Actual Net (o Valor Capital)

#### Definició

El **VAN** actualitza tots els fluxos nets de caixa al moment present (moment zero) i els compara amb el desemborsament inicial. Permet ordenar les inversions per rendibilitat.

#### Fórmula

$$\text{VAN} = -D_0 + \frac{F_1}{(1+i)^1} + \frac{F_2}{(1+i)^2} + \cdots + \frac{F_n}{(1+i)^n}$$

on:
- $D_0$ = desemborsament inicial
- $F_i$ = flux net de caixa de l'any $i$
- $i$ = taxa d'actualització o descompte (tipus d'interès de mercat)
- $n$ = durada de la inversió en anys

#### Criteri de decisió

| Resultat | Decisió | Justificació |
|---|---|---|
| **VAN < 0** | No es fa la inversió | La inversió genera pèrdues: la suma actualitzada de les sortides supera la de les entrades |
| **VAN = 0** | Indiferent | Ni es guanya ni es perd: les entrades i sortides actualitzades s'igualen |
| **VAN > 0** | Es pot fer la inversió | La inversió és rendible: la suma actualitzada de les entrades supera la de les sortides |

> [!IMPORTANT]
> Si s'ha de triar entre diverses inversions amb VAN positiu → **s'escull la que tingui el VAN més alt**.

### TIR — Taxa Interna de Rendibilitat (o Taxa Interna de Retorn)

#### Definició

La **TIR** és la taxa d'actualització ($r$) que fa que el **VAN sigui igual a zero**. Representa la màxima rendibilitat que pot oferir la inversió.

$$0 = -D_0 + \frac{F_1}{(1+r)^1} + \frac{F_2}{(1+r)^2} + \cdots + \frac{F_n}{(1+r)^n}$$

Per decidir si una inversió és viable, es compara la TIR ($r$) amb la taxa d'actualització del mercat ($i$):

#### Criteri de decisió

| Resultat | Decisió | Justificació |
|---|---|---|
| **r < i** | No interessa la inversió | La rendibilitat obtinguda és inferior al tipus d'interès del mercat |
| **r = i** | Indiferent | L'empresa no guanya ni perd; només recupera la inversió |
| **r > i** | Convé fer la inversió | La rendibilitat del projecte supera el cost del finançament |

> [!IMPORTANT]
> Si s'ha de triar entre diverses inversions amb $r > i$ → **s'escull la que tingui la TIR ($r$) més alta**.

---

### Comparativa dels Tres Mètodes

| Criteri | Pay-back | VAN | TIR |
|---|---|---|---|
| **Tipus** | Estàtic | Dinàmic | Dinàmic |
| **Té en compte el temps** | No | Sí | Sí |
| **Mesura** | Temps de recuperació | Valor creat (€) | Rendibilitat (%) |
| **Decisió favorable** | Pay-back mínim | VAN > 0 (màxim) | r > i (màxima r) |
| **Limitació principal** | Ignora el valor temporal del diner i els fluxos posteriors a la recuperació | Requereix conèixer el tipus d'interès $i$ | Pot haver-hi múltiples solucions; no mesura valor absolut |

---

### Resum de Fórmules

$$\text{Pay-back (fluxos iguals)} = \frac{D_0}{F_i}$$

$$\text{VAN} = -D_0 + \sum_{t=1}^{n} \frac{F_t}{(1+i)^t}$$

$$\text{TIR} \Rightarrow \text{VAN} = 0 \Rightarrow -D_0 + \sum_{t=1}^{n} \frac{F_t}{(1+r)^t} = 0$$

---

### Consells per a l'Examen (PAU)

- **Pay-back amb fluxos desiguals**: suma els fluxos any a any; quan la suma acumulada superi $D_0$, calcula la fracció de l'any que falta.
- **VAN**: actualitza cada flux dividint per $(1+i)^t$, on $t$ és l'any corresponent. Suma-ho tot i resta $D_0$.
- **TIR**: a la PAU **no cal calcular-la**, però sí interpretar-la: indica la rendibilitat màxima del projecte i es compara amb el tipus d'interès $i$.
- Recorda que el **valor residual** ($R$) s'afegeix al darrer flux de caixa: $F_n = C_n + R - P_n$.
- Els fluxos de caixa són **cobraments − pagaments**, no ingressos − despeses.
