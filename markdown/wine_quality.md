# Wine Quality

**Summary:** Two datasets are included, related to red and white vinho verde wine samples, from the north of Portugal. The goal is to model wine quality based on physicochemical tests (see [Cortez et al., 2009], http://www3.dsi.uminho.pt/pcortez/wine/).

| Parameter | Value |
| --- | --- |
| **Name** | Wine Quality |
| **Labeled** | Yes |
| **Time Series** | No |
| **Simulation** | No |
| **Missing Values** | No |
| **Dataset Characteristics** | Multivariate |
| **Feature Type** | Real |
| **Associated Tasks** | Classification, Regression |
| **Number of Instances** | 4898 |
| **Number of Features** | 11 |
| **Date Donated** | 2009-10-06 |
| **Source** | UCI Machine Learning Repository |

## Dataset Information

The two datasets are related to red and white variants of the Portuguese 'Vinho Verde' wine. For more details, consult: http://www.vinhoverde.pt/en/ or the reference [Cortez et al., 2009].  Due to privacy and logistic issues, only physicochemical (inputs) and sensory (the output) variables are available (e.g. there is no data about grape types, wine brand, wine selling price, etc.). 
These datasets can be viewed as classification or regression tasks.  The classes are ordered and not balanced (e.g. there are many more normal wines than excellent or poor ones). Outlier detection algorithms could be used to detect the few excellent or poor wines. Also, we are not sure if all input variables are relevant. So it could be interesting to test feature selection methods.

## Tags

Wine quality, Physicochemical analysis, Sensory data, Classification tasks, Regression tasks

## References

- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)

[⬅️ Back to Index](../README.md)