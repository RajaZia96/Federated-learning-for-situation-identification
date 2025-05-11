# Federated-learning-for-situation-identification
This project proposes a federated learning-based framework (FL-SAWCS) to recognize personalized real-world situations using multimodal wearable sensor and contextual data from 60 users. It aims to preserve user privacy, improve generalization, and enhance the recognition of both common and complex activities in a scalable and efficient way.

📌 Objective
To build a privacy-preserving, personalized, and context-aware federated learning system for recognizing real-life situations (e.g., Watching TV, Walking-Talking, Sleeping) using data from smartphones and wearables.

🧠 Key Features
📱 Multimodal Input: Accelerometer, gyroscope, magnetometer, location, audio, and time-of-day features.

🔐 Privacy-Preserving FL: Raw data remains on-device; only model updates are shared.

📊 Graph-Based Personalization: Client similarity graph created using cosine similarity.

⚙️ FL Methods Compared:

FedAvg – Baseline averaging

FedProx – Stability under data heterogeneity

FedPer – Personalized heads

GTVMin – Graph Total Variation Minimization (proposed)

🧮 Architecture Overview
Each user trains a local MLP model on personal data. In the GTVMin approach, each client is a node in a similarity graph. Neighboring users with similar behavior share model information for smooth, robust personalization.

📂 Dataset
Extrasensory Dataset: 60 users

16 situation labels

Labels include daily and complex situations (e.g., Running, Standing-Talking, Lying-Down)

Data split: 70% training, 15% validation, 15% testing per client

⚙️ Training Setup
5 communication rounds

5 local training epochs per round

Evaluation: Accuracy, Precision, Recall, F1-score (macro & weighted)
