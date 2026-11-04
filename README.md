# Ant Colony Optimization aplicado ao Acasalamento Otimizado em Rebanhos Bovinos

Implementação da meta-heurística **Ant Colony Optimization (ACO)** — especificamente o modelo **Ant Colony System (ACS)** — para resolver o problema de acasalamento otimizado em rebanhos bovinos (touros × vacas). 

O objetivo é equilibrar dois critérios conflitantes:
1. **Minimizar a coancestralidade** (parentesco) para preservar a diversidade genética.
2. **Maximizar o ganho genético** esperado da prole por meio de índices de seleção.

Trabalho desenvolvido na disciplina de **Problemas e Algoritmos** (2º semestre de 2025) do curso de Engenharia de Computação da **Universidade Federal do Pampa (UNIPAMPA)**, Campus Bagé.

---

## ⚙️ O Problema e a Modelagem

O problema consiste em definir quais touros cruzar com quais vacas respeitando restrições de uso máximo por macho e evitando endogamia excessiva. 

- **Representação:** Modelado como um grafo bipartido onde formigas artificiais constroem soluções probabilísticas baseadas em **feromônio** (experiência acumulada da colônia) e **heurística** (índices genéticos dos animais).
- **Função de Custo:** Soma das coancestralidades dos casais formados, com critério de desempate baseado na soma dos índices genéticos.
- **Análise de Limites:** O estudo avaliou diferentes limites de acasalamentos por macho (de 12 a 20), identificando por meio de uma função de utilidade que o limite de **15 usos** oferece o melhor equilíbrio entre diversidade e ganho genético.

---

## 📂 Estrutura do Repositório

```text
.
├── aco_apa.ipynb                 # Notebook principal com a implementação
├── parentesco_produtos.csv       # Coeficientes de coancestralidade entre casais
├── pais_indice.csv               # Índices genéticos originais dos animais
├── pais_indice_modificado.csv    # Índices genéticos modificados
├── Ant_Colony_Optimization.pdf   # Slides da apresentação
└── Artigo_ACO/                   # Código-fonte LaTeX do artigo (template IEEE)