# Neural-Architecture-Search-using-Genetic-Algorithm

Task is to create a search algorithm to search in a Neural Architecture
Search (NAS) space for the best performing Convolutional Neural Network
(CNN) architecture on the fashion-mnist data-set. Best performing is de-
fined as having a test accuracy above 75% and the lowest parameter count
model your algorithm can find
CNN Architecture Constraints

Your search algorithm should search for models with the following basic struc-
ture. Sequential model (no skip connections) having the following layers,

• Any number of normal(NC) CNN layers
– torch.nn.Conv2d or tf.keras.layers.Conv2D
– A normal CNN layer has the following constraints,
∗ stride=1
∗ padding=same
∗ 1 <= kernel size < 8
∗ Any of the following activation functions,
· relu
· sigmoid
· tanh
· swish
· gelu

• Exactly 2 reduction(RC) CNN layers
– torch.nn.Conv2d or tf.keras.layers.Conv2D
– A reduction layer has the same constraints as the normal layer except
the following,
∗ stride=2
∗ padding=valid

• Exactly the following structure as the final layers,
– First, a Global Average Pooling 2D layer.
∗ torch.nn.AvgPool2d(kernel size=layer input image size)
or tf.keras.layers.GlobalAveragePooling2D
– Then, a Fully Connected/Dense layer with 64 units (such that output
is shape (batch size, 10)).
∗ This layer can have any of the allowed activations in NC layer
but all final layers must use same activation.
∗ torch.nn.Linear(64) or tf.keras.layers.Dense(64)
– Then, a Fully Connected/Dense layer with 10 units (such that output
is shape (batch size, 10))
∗ This layer can have any of the allowed activations in NC layer
but all final layers must use same activation.
∗ torch.nn.Linear(10) or tf.keras.layers.Dense(10)



For the implementation refer the report
