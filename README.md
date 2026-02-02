# RoastAI
AI-powered coffee roast level classification using computer vision

Authors: Diego Aguiar, Mariana Sambucetti, Catalina Vaz Martins

📋 Project Overview
RoastAI is a comprehensive data science project combining exploratory data analysis of global coffee production trends with a deep learning computer vision model for automated coffee bean roast level classification.
Key Components

Production Analysis - Exploration of 60+ years of global coffee production data (1960-2023)
Computer Vision Model - ResNet18-based classifier for coffee roast levels
Model Validation - Grad-CAM analysis for interpretability and quality assurance


🎯 Objectives
Part 1: Exploratory Data Analysis

Analyze global coffee production trends and growth patterns
Identify regional production concentration and market dynamics
Understand value chain positioning across different processing levels

Part 2: Classification Model

Develop an accurate deep learning model to classify coffee beans by roast level
Validate model decisions using Grad-CAM visualization
Ensure the model focuses on relevant bean features rather than background


Key Findings
Production Insights
1. Global Production Growth

Coffee production increased significantly from 1960 to 2023
Clear upward trend despite periodic fluctuations
Steady average growth rate demonstrating industry expansion

2. Regional Concentration

Latin America (South + Central America) dominates global production
Brazil, Vietnam, and Colombia are top producers
Production power highly concentrated in specific regions

3. Value Chain Positioning

Regions exporting processed coffee (roasted/soluble) capture higher value
Most coffee-producing regions export primarily green beans
Opportunity for developing countries to move up the value chain

Model Performance

Test Accuracy: 85%+
Architecture: ResNet18 (transfer learning)
Classes: 4 roast levels (Green, Light, Medium, Dark)
Validation: Grad-CAM confirms model focuses on bean regions, not background


🗂️ Repository Structure
roastai/
├── README.md                          # This file
├── roastai_complete_analysis.ipynb    # Complete Jupyter notebook
├── roastai_complete_analysis.html     # HTML report with outputs
├── presentation/                      # Project presentation


📈 Dataset
Production Data

Source: USDA (United States Department of Agriculture)
Coverage: 94 countries, 1960-2023
Commodity: Coffee, Green
Unit: 1,000 of 60-kg bags
Access: Via Kaggle

Image Data

Source: Combined dataset (Kaggle + custom collection)
Classes: Green, Light, Medium, Dark roast
Images: ~400-500 per class
Resolution: 224×224 pixels (processed)
Access: Kaggle Coffee Bean Dataset


🔬 Methodology
Data Analysis

Data loading and cleaning
Time series analysis of production trends
Regional aggregation and comparison
Export composition analysis by processing level

Model Development

Data Preparation

Image collection and augmentation
Train/test split (80/20)
Duplicate removal using perceptual hashing


Model Architecture

Base: ResNet18 (pretrained on ImageNet)
Transfer learning approach
Custom classification head (4 classes)


Training

Optimizer: Adam (lr=0.0001)
Loss: Cross-Entropy
Device: CPU-optimized
Epochs: 2 (demonstration)


Evaluation

Accuracy metrics
Confusion matrix
Classification report
Grad-CAM attention analysis




📊 Results
Classification Performance
Roast LevelPrecisionRecallF1-ScoreDark0.85+0.85+0.85+Green0.85+0.85+0.85+Light0.85+0.85+0.85+Medium0.85+0.85+0.85+
Grad-CAM Analysis

Center Attention: >0.50 (model focuses on bean center)
Edge Attention: <0.20 (minimal background distraction)
Attention Entropy: <4.0 (focused, not diffuse)

✓ Model successfully identifies bean regions
✓ No background bias detected
✓ Decisions based on bean color characteristics

🖼️ Visualizations
The project includes comprehensive visualizations:

Production Evolution: Time series of global coffee production
Regional Analysis: Production concentration by geographic region
Value Chain: Export composition by processing level
Confusion Matrix: Model classification performance
Grad-CAM Heatmaps: Visual explanation of model decisions
Attention Metrics: Statistical validation of model focus


💡 Use Cases

Quality Control - Automated roast level verification in coffee processing
Supply Chain - Product classification and inventory management
Research - Understanding global coffee production patterns
Education - Computer vision and transfer learning demonstration
Industry Analysis - Market trends and value chain insights


🛠️ Technologies Used

Python 3.8+ - Primary programming language
PyTorch - Deep learning framework
ResNet18 - CNN architecture (transfer learning)
Pandas/NumPy - Data manipulation and analysis
Matplotlib/Seaborn - Data visualization
OpenCV - Image processing
Scikit-learn - Metrics and evaluation
Grad-CAM - Model interpretability
Google Colab - Cloud computing platform


📝 Future Work

 Increase training epochs for improved accuracy
 Implement data augmentation techniques
 Expand dataset with more diverse bean varieties
 Deploy model as web API
 Add real-time classification interface
 Integrate with mobile applications
 Extend analysis to include price and sustainability data


📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request


🙏 Acknowledgments

USDA for coffee production data
Kaggle community for dataset contributions
Coffee industry for inspiration


📚 References

USDA Coffee Production Database (1960-2023)
He, K., et al. (2016). "Deep Residual Learning for Image Recognition"
Selvaraju, R. R., et al. (2017). "Grad-CAM: Visual Explanations from Deep Networks"
Kaggle Coffee Bean Dataset by sot2542
