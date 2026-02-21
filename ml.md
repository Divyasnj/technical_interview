
Machine Learning works well for structured data and smaller datasets, but it requires manual feature engineering. 
Deep Learning automatically learns features using multi-layer neural networks and performs better on large-scale unstructured data like images, audio, and text.


“There are mainly three types of Machine Learning: Supervised Learning, Unsupervised Learning, and Reinforcement Learning.

In Supervised Learning, the model is trained on labeled data.
In Unsupervised Learning, the model finds patterns in unlabeled data.
In Reinforcement Learning, the model learns by interacting with the environment using rewards and penalties.”

🔹 1️⃣ Supervised Learning

Data is labeled

Has input + correct output

Used for prediction

Examples:

House price prediction (Regression)

Spam detection (Classification)

Algorithms:

Linear Regression

Logistic Regression

Decision Trees

SVM

🔹 2️⃣ Unsupervised Learning

Data is not labeled

Model finds hidden patterns

Examples:

Customer segmentation

Market basket analysis

Algorithms:

K-Means

Hierarchical Clustering

DBSCAN

🔹 3️⃣ Reinforcement Learning

Agent learns by trial and error

Uses reward & punishment mechanism

Examples:

Self-driving cars

Game AI

Robotics




1️⃣ What is Feature Engineering?
🎯 Interview Answer:

“Feature engineering is the process of selecting, transforming, and creating relevant input features from raw data to improve the performance of machine learning models. It helps the model focus on important patterns in the data.”

🔎 Example:

In house price prediction:

Raw data → size, location, age

Engineered features → price per square foot, age category

2️⃣ Why does Deep Learning need more data?
🎯 Interview Answer:

“Deep Learning models have millions of parameters. To properly train these parameters and avoid overfitting, they require large amounts of data. More data helps the model generalize better and learn complex patterns.”

👉 Fewer data = overfitting
👉 More data = better generalization

3️⃣ Why does Deep Learning require GPUs?
🎯 Interview Answer:

“Deep Learning involves heavy matrix multiplications and parallel computations. GPUs are optimized for parallel processing, allowing faster training compared to CPUs.”

👉 Neural networks = matrix operations
👉 GPUs = thousands of cores → faster computation

4️⃣ Difference Between ANN, CNN, and RNN
🎯 Interview Answer:

“ANN is a basic neural network used for structured data.
CNN is designed for image data and captures spatial features using convolution layers.
RNN is designed for sequential data and maintains memory of previous inputs.”

Quick Comparison:
Model	Best For	Special Feature
ANN	Tabular data	Fully connected layers
CNN	Images	Convolution & feature extraction
RNN	Time-series/Text	Sequential memory
5️⃣ Can Deep Learning work with small datasets?
🎯 Interview Answer:

“Yes, but performance may not be optimal. Techniques like transfer learning, data augmentation, and regularization can help improve results when working with small datasets.”

6️⃣ Disadvantages of Deep Learning
🎯 Interview Answer:

Requires large data

High computational cost

Needs GPUs

Hard to interpret (black box model)

Training takes longer

Risk of overfitting
