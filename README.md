# DeepLearningBasedOnPhysics

Repositorio de prácticas de **Aprendizaje Profundo Basado en la Física** con enfoque notebook-first.

## Objetivo

Este repositorio reúne guías y ejercicios sobre:
- Fundamentos de Python/ML con PyTorch
- Autograd y problemas inversos
- PINNs
- Física diferenciable
- Modelos probabilísticos
- Simulation-Based Inference (SBI)
- Flujos normalizantes y GANs

## Estructura

- `/data`: datasets necesarios para ejercicios reproducibles.
- `*.ipynb`: guías y ejercicios principales.
- Artefactos generados (pesos, logs, salidas de entrenamiento): **no se versionan**.

## Ruta sugerida de trabajo

1. `Guia_Semana_01_Fundamentos_Python_y_ML.ipynb`
2. `Guia_Semana_02_Deep_Learning_Autograd.ipynb`
3. `Guia_Semana_03_PINNs.ipynb`
4. `Guia_Semana_04_Fisica_Diferenciable.ipynb`
5. `Guia_Semana_05_Modelos_Probabilisticos.ipynb`
6. `Guia_Semana_06_SBI.ipynb`

Complementarios:
- `Ejercicio19_P1.ipynb`
- `Problema3_P3.ipynb`
- `Ising.ipynb`
- `Ising_GAN.ipynb`
- `MAF.ipynb`

## Instalación mínima

Desde la raíz del repo (`/home/runner/work/DeepLearningBasedOnPhysics/DeepLearningBasedOnPhysics`):

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/macOS
pip install -U pip
pip install -r requirements.txt
```

## Política de notebooks limpios

Este repo versiona notebooks **sin outputs** y con `execution_count = null` para minimizar diffs y costo de tokens.

### Limpieza automática recomendada (pre-commit)

```bash
pip install pre-commit
pre-commit install
pre-commit run -a
```

## Política de artefactos

No versionar:
- Pesos/checkpoints (`*.pth`, `*.pt` generados por entrenamiento)
- Logs de entrenamiento (`sbi-logs/`, TensorBoard events)
- Salidas renderizadas (`*.gif`, figuras temporales)

Estos archivos deben regenerarse localmente o almacenarse externamente (releases/bucket) cuando sea necesario compartir resultados.
