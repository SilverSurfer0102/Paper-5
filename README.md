# Paper 5: Can Perplexity Detect AI-Generated Text?

**Forschungsfrage**: Kann Perplexity als Metrik verwendet werden, um AI-generierten Text von menschlichem Text zu unterscheiden?

**Autoren**: Mimar Sinan Yildiz
**Datum**: Februar 2026

---

## 📂 Ordnerstruktur

```
Paper 5/
├── Aassignment5.pdf               # Original Assignment
├── Human.xlsx                     # Originaldaten (30 Human-Texte)
├── AI.xlsx                        # Originaldaten (30 AI-Texte)
│
├── Paper5_Hauptnotebook.ipynb     # Jupyter Notebook (Hauptausführung)
│
├── data/                          # Verarbeitete Daten
│   ├── human_texts.json           # 30 Human-Texte (JSON)
│   ├── ai_texts.json              # 30 AI-Texte (JSON)
│   └── combined_data.csv          # Alle 60 Texte + Perplexity-Werte
│
├── results/                       # JSON-Ergebnisse der Experimente
│   ├── experiment1_statistics.json
│   ├── experiment2_classification.json
│   └── experiment3_error_analysis.json
│
├── figures/                       # Generierte Plots
│   ├── experiment1_boxplot.png
│   └── experiment2_roc_curve.png
│
└── Figures and Graphics Paper 5/  # Alle Ergebnisse für Paper
    ├── Ergebnisse_Zusammenfassung.md
    ├── experiment1_boxplot.png
    ├── experiment2_roc_curve.png
    └── experiment1-3_*.json
```

---

## 🎯 Hauptergebnisse

### Experiment 1: Statistischer Vergleich
- **Human PPL**: 39.50 ± 23.31
- **AI PPL**: 44.57 ± 21.82
- **t-Test**: t = -0.87, p = 0.389 (NICHT signifikant)
- **Cohen's d**: -0.22 (Negligible)

### Experiment 2: Klassifikation
- **ROC-AUC**: 0.418 (schlechter als Zufall!)
- **Accuracy**: 53.3%
- **F1-Score**: 0.18

### Experiment 3: Error Analysis
- **Korrekt**: 32/60 (53.3%)
- **False Positives**: 1
- **False Negatives**: 27

---

## 💡 Interpretation

**Hypothese NICHT bestätigt**: Perplexity funktioniert NICHT als AI-Detektor.

**Warum?**
1. **Modell-Gap**: GPT-2 (2019) kann ChatGPT-5.2 (2025) nicht erkennen
2. **AI-Qualität**: Moderne AI schreibt "menschlicher"
3. **Umgekehrter Effekt**: AI-Texte haben HÖHERE Perplexity (weniger vorhersagbar)

**Für das Paper**: Negative Ergebnisse sind wissenschaftlich wertvoll!

---

## 🔬 Reproduzierbarkeit

**Jupyter Notebook**:
```bash
jupyter notebook Paper5_Hauptnotebook.ipynb
```

**Dauer**: ~10-30 Minuten

---

## 📊 Für das Paper

**Plots**:
- Figure 1: experiment1_boxplot.png
- Figure 2: experiment2_roc_curve.png

**Tabellen**: Siehe Ergebnisse_Zusammenfassung.md

