# GarbageSegNet

GarbageSegNet is a semantic segmentation project designed to identify and mask garbage areas in images. 
The model highlights garbage (trash) as white, while keeping water, grass, walls, and other backgrounds black.

## Features
- Utilizes depthwise separable convolutions for efficient segmentation.
- Designed for three classes: Garbage, Water, and Background.
- Outputs binary masks where garbage is white, and everything else is black.

## How to Use

1. **Download the Project Files**:  
   - Download the project folder manually or use the provided ZIP file.

2. **Set Up Your Environment**:  
   - Ensure you have the following dependencies installed in your Python environment:  
     ```plaintext
     tensorflow==2.13.0
     keras==2.13.1
     numpy==1.23.5
     opencv-python==4.8.0.76
     scikit-learn==1.3.0
     ```

     Install them using:
     ```bash
     pip install -r requirements.txt
     ```

3. **Prepare the Dataset**:  
   - Place your input images in the folder named `new_x_` and the corresponding label masks in `new_y_`.

4. **Train the Model**:  
   - Run the training script to train the model:  
     ```bash
     python train.py
     ```

5. **Make Predictions**:  
   - Use the `predict_()` function in the code to test the model on new images. Example:
     ```python
     predict_("/path/to/your/image.png")
     ```

## Dependencies
- Python 3.8+
- TensorFlow / Keras
- OpenCV
- NumPy

## Dataset Requirements
- Input images (e.g., `new_x_` folder): RGB images of the scenes.
- Labels (e.g., `new_y_` folder): Grayscale images with three classes:
  - Class 0: Water (Black in ground truth)
  - Class 1: Garbage (Green in ground truth)
  - Class 2: Background (Red in ground truth)

## Example Output
- Garbage (Green)
- Water (Black)
- Background (Red)
