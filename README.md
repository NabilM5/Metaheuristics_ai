# Capacitated VRP with a Hybrid Genetic Algorithm

This repository contains a Hybrid Genetic Algorithm (GA + 2-opt local search) implementation for the Capacitated Vehicle Routing Problem (CVRP) and experiments on CVRPLIB sets E, F, M, P.

**Main Notebook**
`Metaheuristics_ai_Mouhamech_Nabil.ipynb`

## Requirements

- Python 3.9+
- Jupyter or Google Colab
- `matplotlib`, `scipy`, `pandas`, `numpy`
- `7z` for extracting `.7z` archives

The notebook installs missing Python packages automatically at runtime.

## Quick Start

1. Open `Metaheuristics_ai_Mouhamech_Nabil.ipynb`.
2. Run all cells from top to bottom.
3. The notebook will:
   - Extract `E.7z`, `F.7z`, `M.7z`, `P.7z`
   - Parse `.vrp` instances
   - Run the Hybrid GA
   - Compute Gap % vs. optimal values
   - Produce plots for runtime and gap analysis

## Algorithm Summary

- Representation: list of routes, each route is a list of customer indices (depot is index 0).
- Operators: tournament selection, order crossover (OX), swap mutation.
- Local search: 2-opt applied periodically.
- Stopping criterion: fixed number of generations.

## Parameters (Default)

- `pop_size`: 50
- `num_generations`: 200
- `crossover_rate`: 0.8
- `mutation_rate`: 0.1
- `tournament_size`: 5
- `local_search_frequency`: 10

You can change these in the experiment cell in the notebook.

## Evaluation

For each instance, the notebook computes:
- Best distance found
- Optimal distance (from CVRPLIB)
- Gap % = `(best - optimal) / optimal * 100`
- Runtime in seconds

The analysis includes:
- Runtime vs. problem size (scatter plot)
- Average Gap % per instance set (bar chart)

## Project Structure

- `Metaheuristics_ai_Mouhamech_Nabil.ipynb` final cleaned notebook
- `metaheuristics_ai_mouhamech_nabil.py` Python export
- `E.7z`, `F.7z`, `M.7z`, `P.7z` datasets

## Notes

- If `7z` is not installed, install `p7zip` and rerun the extraction cell.
- Optimal values are embedded in the notebook (from CVRPLIB).

## Slides

The notebook includes a 5–7 slide outline. Add your repository link in the last slide cell.

## Presentation

Google Drive presentation link: `<https://docs.google.com/presentation/d/1-XH3mdakVg84d0b8cZ98_YR3V9-ZBZ7XFLbEWcwXB3k/edit?usp=sharing>`
