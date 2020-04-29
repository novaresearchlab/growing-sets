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
-  **num_epochs**:  (*Int*) Epoch for each training set.
</br>
An example with *ResNet_Image_Classifier.ipynb*

```python
num_epochs = 10
k_div=10
batch_size = 400

train_with_growing_sets(x_train, y_train, x_test, y_test, model, sets_method="rogs", data_limit=1000, div=k_div, num_epochs=num_epochs, batch_size=batch_size)
```
Output

```
Method: ROGS - Div: 10 - Epoch: 10
Instant LEN: 100
313/313 [==============================] - 1s 4ms/step - loss: 10.1973 - accuracy: 0.0140
Acc: 0.014000000432133675

...

Instant LEN: 1000
313/313 [==============================] - 1s 4ms/step - loss: 11.0780 - accuracy: 0.0181
Acc: 0.01810000091791153
rogs_accs = [0.014000000432133675, ..., 0.01810000091791153]
rogs_sizes = [100, ..., 1000]
Time elapsed: 0:00:24
```

------------

**Nova Research Lab** @ Yildiz Technical University, Istanbul
