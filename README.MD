# Data-Driven Modeling of Concentric Tube Continuum Robot (CTCR)

This project explores data-driven approaches to model the **kinematics of Concentric Tube Continuum Robots (CTCRs)** using machine learning techniques. The goal is to predict the **tip pose** of the robot based on input parameters using various regression models.

## Reference Dataset

This work is based on the dataset and benchmark introduced in:

> **Grassmann, R. M., Chen, R. Z., Liang, N., & Burgner-Kahrs, J. (2022).**  
> *A Dataset and Benchmark for Learning the Kinematics of Concentric Tube Continuum Robots*.  
> [OpenReview link](https://openreview.net/forum?id=DW9uz_GZ0og)

The dataset includes 100000 joint configurations and corresponding 6-DOF sensor measurements from a three-tube CTCR, captured using an electromagnetic tracking system. It is publicly available on GitHub:

🔗 [CRL-Dataset-CTCR-Pose on GitHub](https://github.com/ContinuumRoboticsLab/CRL-Dataset-CTCR-Pose)

## Models Used

The following regression models were implemented and compared:

- **Linear Regression**  
  A simple baseline model to capture linear relationships between input features and the tip pose.

- **Random Forest Regressor**  
  An ensemble method that builds multiple decision trees and averages their predictions to reduce variance and improve accuracy.

- **Extra Trees Regressor**  
  A more randomized version of Random Forest that introduces additional randomness in the splitting process, often leading to faster training and better generalization.

## Objective

To evaluate and compare the performance of different regression models in predicting the **3D tip pose** of the CTCR from input parameters, using a benchmark dataset.

## Repository Structure

```
├── dataset/              # Dataset files
├── output/               # Plots, metrics, and comparison results
├── ctcr-dmml.ipynb       # Jupyter notebook for exploration and modeling       
├── README.md             # Project overview
└── requirements.txt      # Python dependencies
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/syauqibilfaqih/CTCR-DMML.git
   cd CTCR-DMML
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook to train and evaluate the models.

## Evaluation Metrics

Model performance is evaluated using standard regression metrics such as:

- Mean Absolute Error (MAE) or Error Position (which are equal in this case)
- Error Orientation (refer to the paper for the equation)
- Mean Squared Error (MSE)
- R² Score

## Citation

> Grassmann, R. M., Chen, R. Z., Liang, N., & Burgner-Kahrs, J. (2022).  
> *A Dataset and Benchmark for Learning the Kinematics of Concentric Tube Continuum Robots*.  
> [https://openreview.net/forum?id=DW9uz_GZ0og](https://openreview.net/forum?id=DW9uz_GZ0og)


