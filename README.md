🚀 YOLO Object Detection Training using Ultralytics

This repository demonstrates how to set up, train, and evaluate a YOLO object detection model using the Ultralytics YOLO framework.
The project uses GPU acceleration (CUDA) and trains a YOLO model on a custom dataset hosted via Ultralytics HUB.

📌 Features

Easy setup with pip

Uses Ultralytics YOLO (v8 / YOLO11n)

Automatic hardware & dependency checks

Training with CUDA GPU support

Dataset management via Ultralytics HUB

Real-time logging and checkpoint uploads

High-performance training with AMP & AutoBatch

🛠️ Requirements

Python 3.9+

NVIDIA GPU with CUDA (recommended)

Internet connection (for dataset & model downloads)

📦 Installation

Install Ultralytics and required dependencies:

pip install ultralytics


Verify system setup:

from ultralytics import checks
checks()


You should see output confirming:

Python version

Torch version

CUDA availability

RAM & disk status

⚡ Quick Start (3 Lines)

Train a YOLO model in just 3 lines of code:

from ultralytics import YOLO

model = YOLO("yolo11n.pt")
model.train(data="dataset.yaml", epochs=100, imgsz=640)


Replace dataset.yaml with your dataset configuration file.

🔐 Ultralytics HUB Login (Optional but Recommended)

If you're using Ultralytics HUB datasets or models:

from ultralytics import hub
hub.login("YOUR_API_KEY")


This enables:

Cloud dataset access

Model checkpoint uploads

Training monitoring via HUB dashboard

🧠 Model Details

Model: YOLO11n (lightweight & fast)

Task: Object Detection

Input Size: 640 × 640

Parameters: ~2.6M

GFLOPs: ~6.4

Optimizer: AdamW (auto-selected)

AMP: Enabled

Batch Size: Auto-optimized

📊 Training Output

During training, you’ll see metrics like:

Box Loss

Class Loss

DFL Loss

Precision (P)

Recall (R)

mAP@50

mAP@50–95

All results are saved in:

runs/detect/train/


Includes:

Model weights

Training logs

Label visualizations

Metrics plots

🗂️ Project Structure
├── runs/
│   └── detect/
│       └── train/
├── datasets/
│   └── your-dataset/
├── README.md
└── train.py / notebook.ipynb

🧪 Hardware Used (Example)

GPU: Tesla T4 (15 GB)

CPU: 2 Cores

RAM: ~12.7 GB

CUDA: Enabled

📚 References

Ultralytics YOLO: https://github.com/ultralytics/ultralytics

Documentation: https://docs.ultralytics.com

Ultralytics HUB: https://hub.ultralytics.com

🤝 Contributing

Contributions are welcome!
Feel free to fork this repo, improve the training pipeline, or add new features.

📜 License

This project follows the Ultralytics Open Source License.
Please check the official repository for detailed licensing terms.

🙌 Acknowledgements

Ultralytics Team for YOLO & HUB

Open-source community for continuous support
