This project develops a multi-task deep learning framework for modeling chemical mixture exposures and predicting multiple continuous liver-related health outcomes. The main model is a Transformer-based architecture that treats each chemical exposure as an individual token and uses self-attention to learn exposure–exposure interaction patterns. A multilayer perceptron (MLP) is implemented as a baseline model for comparison.

The framework predicts multiple outcomes simultaneously, including FLI, ALT, AST, GGT, ALP, and Total Bilirubin, using chemical exposure variables and selected covariates such as age, BMI, smoking, alcohol use, income, and education. The pipeline includes data cleaning, median imputation, train-fold-only standardization, five-fold cross-validation, model training, performance evaluation, and attention-based interpretation.

Key Features
	•	Multi-task regression for multiple liver biomarkers
	•	Transformer encoder model for chemical mixture interaction learning
	•	MLP baseline for model comparison
	•	Exposure and covariate separation
	•	Five-fold cross-validation
	•	RMSE, MAE, and R² evaluation metrics
	•	Attention matrix extraction and averaging across folds
	•	Saved predictions, metrics, datasets, and figures for reproducibility

Models Implemented
	1.	Multi-Task Tabular Transformer
	•	Treats each chemical exposure as a token
	•	Uses multi-head self-attention to learn exposure interactions
	•	Adds covariates after exposure pooling
	•	Predicts all outcomes jointly
	2.	Multi-Task MLP Baseline
	•	Uses exposures and covariates as flat input features
	•	Provides a standard neural network comparison model

Outputs

The pipeline automatically saves:
	•	Cleaned data report
	•	Exposure, covariate, and outcome lists
	•	Per-fold predictions
	•	Merged predictions across folds
	•	RMSE, MAE, and R² metrics
	•	Attention matrices
	•	Averaged attention heatmap data

Purpose

This project explores whether Transformer-based self-attention can provide a scalable and interpretable approach for modeling complex chemical mixture effects on health outcomes.
