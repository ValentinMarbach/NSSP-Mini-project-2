# NX-421 Mini-project 2: EMG decoding (group T, variant 3: gradient boosting)

Using surface EMG from NinaPro to decode hand movements (classification) and finger joint angles (regression).

| Part | Data | Task |
|---|---|---|
| 1 | NinaPro DB1, subject 2, `S2_A1_E1.mat` (12 movements) | single-subject classification |
| 2 | NinaPro DB1, 27 subjects, exercise 1 | cross-subject generalisation (LOSO, learning curve) |
| 3 | NinaPro DB8, subject 1, `S1_E1_A1.mat` | regression of joint angles 3, 6, 8, 11, 14 |

Deadline: Thursday 17 December 2026, 16:00 (video ≤ 5 min, report ≤ 5 pages, code).

## Data layout

Datasets are **not** in the repo. Download them and point `data/` to them:

```
data/
├── DB1/   S1_A1_E1.mat … S27_A1_E3.mat   (https://ninapro.hevs.ch/instructions/DB1.html, "Preprocessed" zips)
└── DB8/   S1_E1_A1.mat                    (https://ninapro.hevs.ch/instructions/DB8.html)
```

```bash
ln -s /path/to/your/ninapro data
```

## Code

`code/` holds one notebook per part (`01_single_subject.ipynb`, `02_cross_subject.ipynb`, `03_regression.ipynb`).
Dependencies: numpy, scipy, pandas, matplotlib, scikit-learn.
