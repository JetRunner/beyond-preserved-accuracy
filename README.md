# beyond-preserved-accuracy
Repo for EMNLP 2021 paper "Beyond Preserved Accuracy: Evaluating Loyalty and Robustness of BERT Compression"

<img src="https://user-images.githubusercontent.com/22514219/132096907-1f8f0419-19b8-4bef-8b50-81c3e67cf6f0.png" width="400px">

## How to implement the metrics?

### Probability Loyalty
We recommend the off-the-shelf implementation in `scipy`.
```python
from scipy.spatial import distance
distance.jensenshannon([0.75, 0.2, 0.05], [0.8, 0.1, 0.1])  # softmax prediction of the teacher and student
```

### Label Loyalty
We recommend the off-the-shelf implementation in `sklearn`.
```python
from sklearn.metrics import accuracy_score
accuracy_score([0, 2, 1, 3], [0, 1, 2, 3]) # predicted labels of the teacher and student
```

### Robustness
We use [TextFooler](https://github.com/jind11/TextFooler), please follow the instructions there.

## Citation
```bibtex
@inproceedings{beyond-preserved-accuracy,
    title = "Beyond Preserved Accuracy: Evaluating Loyalty and Robustness of BERT Compression",
    author = "Canwen Xu and Wangchunshu Zhou and Tao Ge and Ke Xu and Julian McAuley and Furu Wei",
    booktitle = {{EMNLP}},
    year = "2021",
}
```
