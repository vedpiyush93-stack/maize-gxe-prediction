# Predicting Maize Yield Across Genotypes and Environments

> Our entry in an international prediction competition, written to be reproduced end to end.

[![Genetics](https://img.shields.io/badge/Genetics-2025-1f4e79?style=flat-square)](https://doi.org/10.1093/genetics/iyae195)

---

**The problem.** A maize variety that performs well in Iowa may do poorly in Texas. Yield depends on the
variety (**genotype**), on the growing conditions (**environment**), and on the interaction between the two — and
that interaction is where the difficulty lives. Predicting it well means a breeder can test fewer varieties in
fewer places.

**The competition.** The Genomes to Fields initiative released years of field trial data and invited teams to
predict yields for unseen genotype-environment combinations. We entered as team **DeepCropVision**. The organisers
compared all entries and published the collective finding — that many different modelling strategies performed
comparably well — in *Genetics*.

## What the code does

Four notebooks forming a linear pipeline. Data preprocessing joins the trial records with weather, soil and
management information. Because field data is inevitably incomplete, a dedicated notebook handles **imputation** of
missing values alongside the train/test split. Hybrid genotype features are constructed separately, since a hybrid
variety derives from two parent lines and needs its own encoding. The modelling notebook then fits and evaluates
the predictors.

## Running it

1. `Data_PreProcessing.ipynb` builds the joined table `final_data_all_with_traits.csv`.
2. `Hybrid_Features.ipynb` adds genotype features for hybrid varieties.
3. `Train_Test_Split_Imputations.ipynb` handles missing values and builds the splits.
4. `Modeling_Script.ipynb` fits and evaluates the models.

## Notes

Notebook outputs are committed, so the figures and result tables render on GitHub without running anything. Competition data is distributed by the Genomes to Fields initiative and is not redistributed here.

Research code from my doctoral work at the University of Nebraska–Lincoln (4 notebooks). Previously hosted at `github.com/Ved-Piyush/DeepCropVision_maizegxeprediction2022`.

## Citation

```bibtex
@article{washburn2025g2f,
  title   = {Global genotype by environment prediction competition reveals that diverse
             modeling strategies can deliver satisfactory maize yield estimates},
  author  = {Washburn, Jacob D. and Varela, Jos\'e I. and Xavier, Alencar and others},
  journal = {Genetics}, volume = {229}, number = {2}, pages = {iyae195}, year = {2025}
}
```

---

**Ved Piyush, PhD** · Statistics, University of Nebraska–Lincoln  
[vedpiyush93@gmail.com](mailto:vedpiyush93@gmail.com) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=657rVYAAAAAJ) · [Website](https://vedpiyush93-stack.github.io)