# ASI_12c_3
Architektury rozwiązań i metodyki wdrożeń SI , grupa 3.

### 👥 Zespół

- s27788 — Lidia Kongiel  
- s27841 — Maria Góral  
- s26786 — Michał Sobieski  
- s24602 — Mateusz Brański  
- s25698 — Bartłomiej Kąkol

## 🎯 Cel projektu

Celem projektu jest stworzenie end-to-end systemu ML zgodnie z podejściem MLOps 
— od danych, przez pipeline, aż po API i dashboard.

## 📊 Wybrany problem ML

**Problem:** Klasyfikacja satysfakcji pasażerów linii lotniczych  
**Typ:** Klasyfikacja binarna  
**Cel:** Przewidzieć, czy pasażer jest zadowolony (`satisfied`) czy niezadowolony (`neutral/dissatisfied`)

---

## 📁 Zbiór danych

- Źródło: Kaggle  
- Dataset: Airline Passenger Satisfaction  
- Link: https://www.kaggle.com/datasets/mysarahmadbhat/airline-passenger-satisfaction  

**Charakterystyka:**
- Dane tabelaryczne
- ponad 100 000 obserwacji
- Zmienne: demografia, klasa podróży, opóźnienia, oceny usług

---

## Sprint 1

Zrealizowane elementy:

- ✔ Ingest danych z CSV do SQLite (`data/01_raw/*.sqlite`)
- ✔ Eksploracyjna analiza danych (EDA) – min. 5 wizualizacji:
    - rozkład targetu
    - histogram cechy numerycznej
    - boxplot względem targetu
    - rozkład cechy kategorycznej
    - macierz korelacji
- ✔ Podział danych: train / validation / test (70/15/15)
- ✔ Pipeline preprocessing (imputacja + one-hot encoding)
- ✔ Model baseline: `RandomForestClassifier`
- ✔ Ewaluacja modelu (accuracy, precision, recall, F1, ROC-AUC)
- ✔ Zapis metryk do pliku JSON (`reports/metrics/baseline_metrics.json`)

---

## Uruchomienie
### 1. Przygotuj środowisko (np. conda lub venv)

#### conda
```bash
conda create -n <env_name> python=3.10
conda activate <env_name>
pip install -r requirements.txt
```
---
