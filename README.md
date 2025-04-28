# GTT Minimal Inference Code

This repository provides minimal code for running inference with GTT small-scale models, intended for conceptual experimentation.  
The complete version is under internal review and will be released later.

## Getting Started

### Install Dependencies
> Requires **Python 3.10**.

```bash
pip install -r requirements.txt
```

## Running Experiments

### Zero-Shot Inference
```bash
cd src
python test_zeroshot.py --gpu [GPU_IDs] --batch_size [BATCH_SIZE] --mode [MODEL_SIZE] --data [DATASET] --uni [UNI_FLAG]
```
- `mode`: `tiny`, `small`, or `large`
- `data`: `m1`, `m2`, `h1`, `h2`, `electricity`, `weather`, `traffic`, `ill`
- `uni`: `0` for multivariate forecasting, `1` for univariate forecasting

### Fine-Tuning
```bash
cd experiments
python test_finetune.py --gpu [GPU_IDs] --batch_size [BATCH_SIZE] --mode [MODEL_SIZE] --data [DATASET] --uni [UNI_FLAG] --epochs [EPOCHS]
```

## Using GTT Models on Your Own Data

GTT models support zero-shot forecasting on custom datasets (even on CPU).  
Refer to the [tutorial](./tutorial.ipynb) for detailed usage instructions.
