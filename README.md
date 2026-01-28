roduct Classification using GraphSAGE on Amazon Computers
This project implements a Graph Neural Network (GNN) to solve a multi-class classification problem on a medium-scale e-commerce dataset. The goal is to predict the category of a product based on its features and its relationship with other frequently co-purchased items.

🚀 The Real-World Problem
In e-commerce, automated product categorization is vital for searchability and recommendation. Traditional models often only look at product descriptions (text). This project leverages Relational Data—using the fact that similar products are often bought together—to improve classification accuracy.

📊 Dataset: Amazon Computers
Nodes (13,752): Individual products.

Edges (491,722): Represent products that are "frequently bought together."

Features: Bag-of-words representation of product reviews.

Classes: 10 distinct product categories.

🧠 Model Architecture: GraphSAGE
Unlike standard GCNs, this project utilizes GraphSAGE (SAGEConv). It is chosen for its:

Scalability: Efficiently handles the dense connections in co-purchase graphs.

Inductive Learning: Learns an aggregation function (mean) rather than a simple average, making it more robust to noisy feature data.

Dropout Regularization: Included to prevent overfitting on highly connected nodes.

📈 Performance & Evaluation
The model is evaluated using two key metrics:

Accuracy: Overall percentage of correct predictions.

Macro F1-Score: Used to ensure the model performs well across all categories, even the rare ones (addressing class imbalance).
