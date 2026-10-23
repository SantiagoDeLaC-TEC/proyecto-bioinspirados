# Réplica de Tao et al. (2022) en Hanoi: NSGA-II y NSGA-III

Réplica del caso Hanoi de Tao, Yan, Yang, Ma y Kou (2022), *Multi-objective optimization of water distribution networks based on non-dominated sequencing genetic algorithm*, PLOS ONE 17(11): e0277954. https://doi.org/10.1371/journal.pone.0277954

Optimiza el diámetro de las 34 tuberías de la red Hanoi con tres objetivos (costo, suma y varianza de la cabeza excedente) usando NSGA-II y NSGA-III, con 30 corridas por algoritmo, y compara con el paper (mínimos, Hypervolume, Spacing y prueba de Wilcoxon).

## Requisitos

- Python 3.12
- [uv](https://docs.astral.sh/uv/) (recomendado) o pip

Dependencias principales: WNTR (EPANET), pymoo, numpy, pandas, scipy, matplotlib y Jupyter.

## Instalación

Con uv:

```bash
uv sync
```

## Ejecución

Abrir y ejecutar el notebook completo:

```bash
uv run jupyter notebook notebooks/replicacion_hanoi.ipynb
```

El notebook corre las 60 simulaciones (30 por algoritmo, semillas 1 a 30, población 100, 100 generaciones) y calcula las métricas, las pruebas y las figuras. Los resultados quedan en `results/notebook/`.

**Tiempo:** unos 27 minutos en serie.

## Estructura

```
data/        red Hanoi (hanoi.inp) y tablas del paper
docs/        paper
notebooks/   replicacion_hanoi.ipynb (todo el flujo)
results/     salidas de las corridas, tablas y figuras
```
