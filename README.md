# AutoML in HR

Code for the tutorial:

[AutoML in HR: Predict Employee Attrition with a Built-In Fairness Report](https://mljar.com/tutorials/automl-hr-employee-attrition-fairness-report/)

This project shows how to use **AutoML** to predict employee attrition and check model fairness for the `Gender` feature.

## What is inside?

The main notebook is:

```text
automl-HR.ipynb
```

It shows how to:

* load HR employee attrition data,
* define `Attrition` as the target,
* train models with AutoML,
* compare models on the leaderboard,
* inspect feature importance,
* check fairness metrics for Gender.

## Best Model

AutoML trained several models. The best selected model was:

```text
3_Linear
```

The Linear model is useful because it has good performance and is easier to explain than many complex models.

## Fairness

The notebook checks fairness for the `Gender` feature.

The model has similar selection rates:

```text
Male:   0.1196
Female: 0.1121
```

The Demographic Parity Ratio is:

```text
0.9373
```

The model passed the fairness check with threshold `0.8`.

## Install and Run

```bash
git clone https://github.com/pplonski/automl-in-hr.git
cd automl-in-hr

python -m venv venv
source venv/bin/activate   # macOS/Linux
# venv\Scripts\activate    # Windows

pip install -U pip
pip install pandas mljar-supervised jupyter

jupyter notebook automl-HR.ipynb
```

## Note

Machine learning in HR should be used carefully. The model can support HR analysis, but it should not make automatic decisions about employees.

## License

MIT
