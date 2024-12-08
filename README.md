# Hydroponic Development Stage Classifier

We created a classification solution to identify hydroponic crop development stages using the Roboflow platform.

## Project Goal

The goal is to remotely monitor the development stages of hydroponic farming systems in Brazil's northeastern semi-arid region, aiming to increase productivity and sustainability in dry areas.

The development stages considered are:
- **Early**: Initial stage.
- **Growth**: Vegetative growth.
- **Maturity**: Fully developed stage.
- **Harvest**: Ready for harvest.

---

## Dataset

### Dataset Details
- **Total Images**: 1,147
- **Train Set**: 1,076 images (94%)
- **Validation Set**: 48 images (4%)
- **Test Set**: 23 images (2%)

The dataset is stored in the `data/` folder and includes:
- **COCO JSON File**: `data/coco_annotations.json`
- **Images Folder**: `data/images/`

### Using the Dataset
1. **Download the Repository**:
   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-repo-name/hydroponic-classifier.git
   cd hydroponic-classifier
   ```

2. **Access the Dataset**:
   - The dataset annotations are in the `data/coco_annotations.json` file.
   - The corresponding images are located in the `data/images/` folder.

---

## Annotation Instructions

1. **Annotation Process**:
   - Use a polygon annotation tool to outline the hydroponic crops in each image.
   - Assign one of the following classes to each region:
     - `early` (Early stage)
     - `growth` (Growth stage)
     - `maturity` (Mature stage)
     - `harvest` (Ready for harvest)

2. **Preprocessing**:
   - Images are resized to 640x640 pixels for training.
   - Brightness adjustments are applied randomly between -15% and +15%.

---

## Model Training and Evaluation

The YOLOv11 model was trained using the Roboflow interface. Below are the metrics and graphs from training, validation, and testing:

### Training Metrics:
- **mAP (Mean Average Precision)**: **96.0%**
- **Precision**: **91.4%**
- **Recall**: **88.1%**

### Validation Metrics:
- **mAP**: 94.8%
- **Precision**: 89.7%
- **Recall**: 86.5%

### Testing Metrics:
- **Accuracy**: 88.8%

### Performance Graphs:
- **mAP over Epochs**:
  ![mAP Graph](results/map.png)
- **Object Loss**:
  ![Object Loss Graph](results/object_loss.png)
- **Class Loss**:
  ![Class Loss Graph](results/class_loss.png)
- **Box Loss**:
  ![Box Loss Graph](results/box_loss.png)

---

## How to Reproduce

1. **Set Up the Environment**
   Install the required dependencies using:
   ```bash
   pip install -r requirements.txt
   ```

2. **Access the Dataset**
   Use the dataset provided in the `data/` folder.

3. **Train the Model**
   - Use the Jupyter notebook in `notebooks/training.ipynb` for model training.
   - Alternatively, replicate training using YOLOv11 on your local machine.

4. **Evaluate the Model**
   - Use the notebook in `notebooks/evaluation.ipynb` to visualize metrics and predictions.

---

## Results

### Visualizations:
**Sample Annotation**:
![Sample Annotation](screenshots/sample_annotation.png)

**Sample Prediction**:
![Sample Prediction](results/predictions_sample.png)

---

## License
This project is licensed under the [MIT License](LICENSE).

## Contributors
- **Carolina Bez**: Head of Data Analytics.
- **Klaus Egewarth**: Agricultural Engineer.
- **Otniel Amorim**: Product Manager.

---

### References
- [AI4GOOD](https://ai4good.org/)
```

---

### Resumo das Alterações:
1. **Dataset no Repositório**:
   - Substituímos a dependência da API Roboflow por arquivos diretamente acessíveis no repositório.
2. **Organização de Arquivos**:
   - Adicionamos `coco_annotations.json` e as imagens no subdiretório `data/`.
3. **Atualização no README**:
   - Substituímos as instruções de download via API por instruções para acessar os dados do repositório.

Se precisar de mais ajustes, é só avisar! 😊
