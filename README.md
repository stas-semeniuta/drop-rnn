#### Recurrent Dropout without loss of Memory

Theano code for the Penn Treebank language model and Temporal Order experiments in the paper [Recurrent Dropout without loss of Memory](link).

#### Requirements

**Theano** is required for running the experiments:

```bash
pip install Theano
```

#### Language Modeling Experiments

Select model to run in config.py, then run main.py.

To run the baseline models:
```bash
python -u main.py
```

To run the models with 0.25 per-step dropout in hidden states:
```bash
python -u main.py --hid_dropout_rate 0.25 --per_step
```

To run the models with 0.5 per-sequence dropout in hidden state updates:
```bash
python -u main.py --hid_dropout_rate 0.5 --drop_candidates
```

#### Temporal Order Experiments

To run the baseline LSTM without dropout:
```bash
python -u order.py
```

To run the models with 0.5 per-step dropout in hidden state updates on 30 symbol long sequences:
```bash
python -u order.py --hid_dropout_rate 0.5 --drop_candidates --per_step --low 10 --high 20 --length 30
```