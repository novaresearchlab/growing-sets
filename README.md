# growing-sets
This project is implementation of growing sets methods on Convolutional Neural Network, Long Short-Term Memory and Residual Neural Network architectures.


Methods:
- **SPL**: Self Paced Learning
- **SPLI**: Self Paced Learning-Inversed
- **ROGS**: Random Ordered Growing Datasets

Function call:
```python
train_with_growing_sets(X_train, Y_train, X_test, Y_test, model, sets_method=None, data_limit=None, div=16, num_epochs=30, batch_size=128)
```

Parameters:
-   **sets_method**:  (*String*) Name of the growing sets method you want the train with. e.g. "SPL", "SPLI", "ROGS", "BASE"
-  **data_limit**: (*Int*) If you dont want to feed the model with all of your data, you can limit it.
-  **div**:  (*Int*) How many pieces you want to split your data. Those pieces will add up together in every step.
- **num_epochs**:  (*Int*) Epoch for each training set.

------------

**Nova Research Lab** @ Yildiz Technical University, Istanbul
