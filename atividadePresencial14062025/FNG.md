# Atividade Presencial 14-06-2025

**Transforme a gramática G para FNC e FNG.**

**GLC G = ({S, A, B, C, D, E, F}, {w, x, y, z}, P, S) onde P:**

- **S → AxCy | C | zBAw**
- **A → ESw | zAyC | x**
- **B → CwE | Exy | BFA**
- **C → yAxy | BDw | ε**
- **D → SyzA | wEy | x**
- **E → FxzB | DSE**
- **F → Dy | CS | SBz**

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

4. Eliminar Recursão à Esquerda

- X1 -> xyX2X4 | wzX2X3 | xyX2 | wX3X5 | palavra vazia
- X2 -> wX4X6 | xyX6 | X2X3X7
- X3 -> wX4X6 | xyX6 | X2X3X7
- X4 -> xyyX2 | wX3X5
- X5 -> yzX2X1 | wyX6 | x | yzX2
- X6 -> xzX3X7 | X1X5X6 | X5X6
- X7 -> yX5 | X1X4 | zX1X3 | xyX2X4 | wzX2X3 | xyyX2 | wX3X5

5. Eliminar recursões

- X1 -> xyX2X4 | wzX2X3 | xyX2 | wX3X5 | palavra vazia
- X2 -> wX4X6 | xyX6 | X2X3X7
- X3 -> wX4X6 | xyX6 | X2X3X7
- X4 -> xyX_yX2 | wX3X5
- X5 -> yzX2X1 | wyX6 | x | yzX2
- X6 -> xzX3X7 | X1X5X6 | X5X6
- X7 -> yX5 | X1X4 | zX1X3 | xyX2X4 | wzX2X3 | xyX_yX2 | wX3X5
- X_y -> y

