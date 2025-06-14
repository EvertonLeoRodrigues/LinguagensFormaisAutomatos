# Atividade Presencial 14-06-2025

**Transforme a gramática G para FNC e FNG.**

**GLC G = ({S,A,B,C,D,E,F}, {w,x,y,z} P, S) onde P:**

**S -> AxCy | C | zBAw**

**A -> ESw | zAyC | x**

**B -> CwE | Exy | BFA**

**C -> yAxy | BDw | palavra vazia**

**D -> SyzA | wEy | x**

**E -> FxzB | DSE**

**F -> Dy | CS | SBz**

---

1. Eliminar produções vazias

- S -> AxCy | C | zBAw
- A -> ESw | zAyC | x
- B -> CwE | Exy | BFA
- C -> yAxy | BDw | palavra vazia
- D -> SyzA | wEy | x
- E -> FxzB | DSE
- F -> Dy | CS | SBz

---

- S -> AxCy | C | zBAw | Axy | palavra vazia

- A -> ESw | zAyC | x | zAy
- B -> CwE | Exy | BFA
- C -> yAxy | BDw
- D -> SyzA | wEy | x | yzA
- E -> FxzB | DSE | DE
- F -> Dy | CS | SBz | S | C

2. Eliminar produções unitárias

- S -> AxCy | C | zBAw | Axy | palavra vazia
- A -> ESw | zAyC | x | zAy
- B -> CwE | Exy | BFA
- C -> yAxy | BDw
- D -> SyzA | wEy | x | yzA
- E -> FxzB | DSE | DE
- F -> Dy | CS | SBz | S | C

---

- S -> AxCy | zBAw | Axy | yAxy | BDw | palavra vazia

- A -> ESw | zAyC | x | zAy
- B -> CwE | Exy | BFA
- C -> yAxy | BDw
- D -> SyzA | wEy | x | yzA
- E -> FxzB | DSE | DE
- F -> Dy | CS | SBz | AxCy | zBAw | yAxy | BDw

3. Eliminar símbolos inúteis

> Não há símbolos inúteis

4. Transformação do lado direito das produções de comprimento maior ou igual a dois e transformação do lado direito das produções em exatamente duas variáveis.

- S -> AxCy | zBAw | Axy | yAxy | BDw | palavra vazia
- A -> ESw | zAyC | x | zAy
- B -> CwE | Exy | BFA
- C -> yAxy | BDw
- D -> SyzA | wEy | x | yzA
- E -> FxzB | DSE | DE
- F -> Dy | CS | SBz | AxCy | zBAw | yAxy | BDw

---

- Parte 1

    - S -> AX_xCX_y | X_zBAX_w | AX_xX_z | X_yAX_xX_y | BDX_w | palavra vazia
    - A -> ESX_w | X_zAX_yC | X_x | X_zAX_y
    - B -> CX_wE | EX_xX_y | BFA
    - C -> X_yAX_xX_y | BDX_w
    - D -> SX_yX_zA | X_wEX_y | X_x | X_yX_zA
    - E -> FX_xX_zB | DSE | DE
    - F -> DX_y | CS | SBX_y | AX_xCX_y | X_zBAX_w | X_yAX_xX_y | BDX_w
    - X_w -> w
    - X_x -> x
    - X_y -> y
    - X_z -> z

- Parte 2
    - S -> X1X2 | X3X4 | X1X_z | X5X6 | BX7 | palavra vazia
    - A -> EX8 | X9X10 | X_x | X9X_y
    - B -> CX11 | EX6 | BX12
    - C -> X5X6 | BX7
    - D -> X13X9 | X11X_y | X_x | X_yX9
    - E -> X14X3 | DX15 | DE
    - F -> DX_y | CS | SX16 | X1X2 | X3X4 | X5X6 | BX7
    - X_w -> w
    - X_x -> x
    - X_y -> y
    - X_z -> z
    - X1 -> AX_x
    - x2 -> CX_y
    - x3 -> X_zB
    - x4 -> AX_w
    - X5 -> X_yA
    - X6 -> X_xX_y
    - X7 -> DX_w
    - X8 -> SX_w
    - X9 -> X_zA
    - X10 -> X_yC
    - X11 -> X_wE
    - X12 -> FA
    - X13 -> SX_y
    - X14 -> FX_x
    - X15 -> SE
    - X16 -> BX_y
