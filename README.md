# hydroponic-ai

# Hydroponic Development Stage Classifier

We created a classification solution to identify hydroponic crop development stages using the Roboflow platform.

## Project Objective

The goal is to remotely monitor the development stages of hydroponic farming systems in Brazil's northeastern semi-arid region, aiming to increase productivity and sustainability in dry areas.

The development stages considered are:
- **Early**: Initial stage.
- **Growth**: Vegetative growth.
- **Maturity**: Fully developed stage.
- **Harvest**: Ready for harvest.

---

## Project Setup

### Dataset
The dataset is open-source and available via Roboflow:
- **Download link**: [Hydroponic AI Dataset](https://public.roboflow.com/dataset-url)

### Pipeline
1. **Data Collection**: Images were manually collected from the farming systems (72/day, 500 total).
2. **Annotation and Classification**: Stages were labeled using the Roboflow interface.
3. **Model Training**: YOLOv11 was used on the Roboflow platform.
4. **Validation and Testing**:
   - Mean Average Precision (mAP): **96%**
   - Precision: **91.4%**
   - Recall: **88.1%**

### Dataset Structure
- **Training Set**: 170 images
- **Validation Set**: 49 images
- **Test Set**: 18 images

---

## Model Results

### Performance Metrics
- **mAP (Mean Average Precision)**: 96.0%
- **Precision**: 91.4%
- **Recall**: 88.1%

### Visualizations
**Confusion Matrix**:
![Confusion Matrix](results/confusion_matrix.png)

**Sample Predictions**:
![Predictions Sample](results/predictions_sample.png)

---

## How to Reproduce

### 1. Download the Dataset
Download the dataset from the link provided and place it in the `data/` directory.

### 2. Set Up the Environment
Ensure the dependencies are installed using:
```bash
pip install -r requirements.txt
```

### 3. Train the Model
Open the `training.ipynb` notebook and execute the cells to train the model.

### 4. Evaluate the Model
Use the `evaluation.ipynb` notebook to generate metrics and visualize predictions.

---

## Future Improvements
- IoT integration for automated image collection.
- Expansion to real-time monitoring capabilities.
- Use of unsupervised learning techniques for anomaly detection.

---

## License
This project is licensed under the [MIT License](LICENSE).

## Contributors
- **Carolina Bez**: Head of Data Analytics.
- **Klaus Egewarth**: Agricultural Engineer.
- **Otniel Amorim**: Product Manager.

---

### References
- [Roboflow](https://roboflow.com/)
- [AI4GOOD](https://ai4good.org/)
```
