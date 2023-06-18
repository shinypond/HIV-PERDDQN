# HIV-PERDDQN
This repository provides the official implementation of "An Efficient Deep Q Learning Method to Find the Optimal STI Controls for HIV Patients" (PER-DDQN).

## Setup

### Requirements
This repository has been tested on Python 3.10 and Pytorch 2.0.0.
Other packages are listed in [requirements.txt](./requirements.txt).

Example installation:
```
 pip install -r requirements.txt
```

### Run
Both training and evaluation of PER-DDQN model are conducted by [main.py](./main.py).

---
#### Training
```
 python main.py --exp any_name
```
---
#### Evaluation
```
 python main.py --exp any_name --mode test
```
---

If you change the configuration, see [configs.py](./configs.py) and change some hyperparameters as you want.

For five-day segments setup, set the line 5 and 6 in [configs.py](./configs.py) as follows:
```
 max_days = 1000
 treatment_days = 5
```

For one-day segments setup, set the line 5 and 6 in [configs.py](./configs.py) as follows:
```
 max_days = 600
 treatment_days = 1
```

If you want to verify or change the HIV dynamics environment, see [envs/constants.py](./envs/constants.py).


