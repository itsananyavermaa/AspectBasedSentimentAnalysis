# AspectBasedSentimentAnalysis
This project implements a deep learning pipeline for **Aspect-Based Sentiment Analysis (ABSA)** using a BiLSTM model enhanced with **aspect markers** (`[ASP]...[/ASP]`) to focus attention on specific aspects of user reviews. The model is trained on the [FABSA dataset](https://www.sciencedirect.com/science/article/pii/S0925231223009906?via%3Dihub), which contains fine-grained customer reviews from the Google Play and Apple App Stores across various industries like Fashion, Travel, and Consulting.

### Highlights

- Aspect-Based Sentiment Classification using BiLSTM
- Injected `[ASP]...[/ASP]` markers to focus model attention on target aspects
- Achieved ~92% classification accuracy across 3 sentiment classes (positive, neutral, negative)
- Supports multi-aspect inference within a single sentence
- Clean preprocessing, label encoding, and padded sequence generation pipeline

Each sentence in the dataset is annotated with:
- **Text**: the full customer review
- **Aspect**: fine-grained topics such as `account-management.account-access`, `logistics-rides.speed`, etc.
- **Label**: sentiment polarity (`positive`, `neutral`, or `negative`) for that aspect

The goal of this project is to predict the sentiment expressed toward a **specific aspect** mentioned in a user review.
