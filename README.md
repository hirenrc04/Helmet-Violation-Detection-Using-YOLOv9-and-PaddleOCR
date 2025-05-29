# Helmet-Violation-Detection-Using-YOLOv9-and-PaddleOCR
This project detects helmet violations using a custom-trained YOLOv9 model for object detection and PaddleOCR for license plate recognition.

## 📁 Project Structure

- **helmet-violations.ipynb** — Main notebook for data mounting, YOLOv9 training, and PaddleOCR integration.
- **Dataset** — Loaded from Google Drive, structured with a `data.yaml` file specifying classes:
      - `WithHelmet`
      - `WithoutHelmet`
      - `Plate`

## 📌 Features

- Detects riders with and without helmets.
- Uses YOLOv9 for accurate object detection.
- Integrates PaddleOCR to extract license plate numbers from violators.

## 🔧 Requirements

- Python 3.8+
- Jupyter Notebook or Google Colab
- Required libraries (install via terminal):
      ```bash
      pip install paddleocr opencv-python-headless torch torchvision torchaudio
      ```

## 🛠 Usage

1. **Mount Google Drive to access the dataset:**
       ```python
       from google.colab import drive
       drive.mount('/content/drive')
       ```
2. **Set dataset path and load `data.yaml`:**
       ```python
       dataset_path = '/content/drive/My Drive/Colab Notebooks/dataset/HelmetViolationsV2'
       ```
3. **Train the YOLOv9 model** using your dataset.
4. **Run detection** on images or videos to identify:
       - Riders without helmets
       - Their vehicle’s license plate
5. **Apply PaddleOCR** on detected plates to extract text.

## 📊 Results

- Accurate detection of helmet use/non-use.
- OCR output for license plates integrated with detection results.

## 📷 Sample Output

- Images with bounding boxes:
      - Helmeted riders (green)
      - Violators (red)
      - License plates (blue)
- Extracted plate numbers printed or logged with detections.

## 🚀 Future Improvements

- Automate alert system for identified violators.
- Deploy as a real-time traffic monitoring solution.
- Integrate with vehicle registration databases.

## 📜 License

This project uses a Private license as defined in the Roboflow dataset.

## 🔗 Dataset Info

- Provided by Roboflow
- Project: `helmetviolations`
- Workspace: `helmet-nztej`
- [Roboflow Datasets](https://roboflow.com/)

## 🌐 References

- [YOLOv9 Official Repository](https://github.com/WongKinYiu/yolov9)
- [PaddleOCR Documentation](https://github.com/PaddlePaddle/PaddleOCR)
- [Roboflow](https://roboflow.com/)

---

💬 For questions or contributions, please open an issue or contact the maintainer.
