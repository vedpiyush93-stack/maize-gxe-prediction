# Maize Genotype-by-Environment Yield Prediction

> Our Genomes-to-Fields G×E competition entry, written to be reproduced end to end.

[![Genetics](https://img.shields.io/badge/Genetics-2025-1f4e79?style=flat-square)](https://doi.org/10.1093/genetics/iyae195)

---

Entered as team **DeepCropVision** in the Genomes to Fields Genotype by Environment Prediction
Competition. The competition compared modelling strategies across many independent teams; the collective
finding — that diverse strategies all deliver satisfactory yield estimates — was published in *Genetics* (2025).

Genotype-by-environment prediction is a variance-decomposition problem wearing a machine-learning costume:
yield depends on genotype, on environment, and on an interaction that is exactly where the difficulty lives.

## Reproducing the results

1. `Data_PreProcessing.ipynb` builds `final_data_all_with_traits.csv`, joining training and test features for every data type except genotype hybrids.
2. `Hybrid_Features.ipynb` adds the genotype hybrid features.
3. The remaining notebooks train and evaluate the models.

## Notebooks

**4 notebooks**, committed with their outputs intact so every figure and result table renders on GitHub without re-running anything.

- `Data_PreProcessing.ipynb`
- `Hybrid_Features.ipynb`
- `Modeling_Script.ipynb`
- `Train_Test_Split_Imputations.ipynb`

## Related publications

- [Genetics 229(2), iyae195](https://doi.org/10.1093/genetics/iyae195)

## Citation

```bibtex
@article{washburn2025g2f,
  title   = {Global genotype by environment prediction competition reveals that diverse
             modeling strategies can deliver satisfactory maize yield estimates},
  author  = {Washburn, Jacob D. and Varela, Jos\'e I. and Xavier, Alencar and others},
  journal = {Genetics}, volume = {229}, number = {2}, pages = {iyae195}, year = {2025}
}
```

## About this repository

Research code from my doctoral work at the University of Nebraska–Lincoln. Trained model checkpoints and bulk datasets are excluded from version control; the notebooks regenerate them. Previously hosted at `github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022`.

---

**Ved Piyush, PhD** · Statistics, University of Nebraska–Lincoln  
[vedpiyush93@gmail.com](mailto:vedpiyush93@gmail.com) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=657rVYAAAAAJ) · [LinkedIn](https://www.linkedin.com/in/ved-piyush)