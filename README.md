# 🌳 Real-Time Tree Detector

A real-time tree detection and counting system using YOLOv11, built for use in forestry, environmental monitoring, and urban planning. Supports live camera feeds and pre-recorded videos with CLI and optional GUI.

<!-- <p align="center">
  <img src="docs/demo.gif" alt="Tree Detection Demo" width="600"/>
</p> -->

---

## 🚀 Features

- ⚡ Fast, accurate detection with [YOLOv11](https://docs.ultralytics.com)
- 🎥 Support for video files and real-time camera feeds (USB/RTSP)
- 📊 Real-time counting with visual overlay
- 🧩 Modular codebase (Hydra config, CLI, model abstraction)
- 🖥️ Optional GUI (Streamlit/FastAPI)
- 🧪 Unit tests + CI + logging
- 📦 Exportable to ONNX/TensorRT for edge deployment

---

## 📸 Demo

```bash
# Run detection on webcam feed
python inference/live_camera_detection.py detect --source 0 --model yolov11s.pt

# Run on video file
python inference/video_file_detection.py detect --source ./samples/forest.mp4
```

> 💡 Want to try it now? [Click here to run on Colab](https://colab.research.google.com/...)

---

## 📂 Project Structure

```text
tree-detector/
├── models/          # YOLOv11 wrapper
├── dataset/          # pre-precessed dataset
├── training/          # Training notebook
├── inference/       # API Based Stream/video processing
├── tracking/        # Object tracking (e.g., ByteTrack)
│   ├── cli.py           # Typer-based CLI
│   └── gui/             # Optional GUI
├── tests/               # Unit and integration tests
├── scripts/             # Training, export, benchmarking
├── docs/                # Documentation
├── requirements.txt
├── pyproject.toml
└── README.md
```

---

## 📋 Prerequisites

Before installing the project dependencies, you need to install the `uv` package manager:

---

## 🛠️ Installation

```bash
# Clone repository
git clone https://github.com/yourusername/tree-detector.git

# Create virtual environment and Install dependencies
uv sync
```

---

## 🧪 Quick Start

1. **GUI (optional):**

   ```bash
   streamlit run tree_detector/gui/app.py
   ```

---

## 🧠 Model Info

- Backbone: YOLOv11‑s (default), modular for upgrades
- Supported formats: `.pt`, `.onnx`, `.engine` (TensorRT), `.xml` (OpenVINO)
- FPS: 30+ real-time on RTX 4060

---

## 📈 Datasets

> To train or fine-tune your own model, see [`scripts/train.py`](scripts/train.py)

This project utilizes and supports various open-source tree detection datasets:

### 🌱 **Included Datasets**

- **Tree-Top-View Dataset** - Drone aerial imagery for tree detection
  - Source: [Roboflow Tree Dataset](https://universe.roboflow.com/treedataset-clsqo/tree-top-view)
  - License: CC BY 4.0
  - Format: YOLOv11 with 1,384 images
  - Classes: `tree-top` (single class)

### 📊 **Dataset Statistics**

| Dataset | Images | Classes | Resolution | Use Case |
|---------|--------|---------|------------|----------|
| Tree-Top-View | 1,384 | 1 | 416×416 | Drone monitoring |

### 🔗 **Data Preparation**

- [Data preparation docs](docs/data-prep.md)
- [Dataset conversion scripts](scripts/)
- [Training configuration examples](training/)

---

## 🧪 Testing & Development

```bash
# Run unit tests
pytest

# Check code style
pre-commit run --all-files
```

---

## 📦 Deployment

We support:

- **Docker**  

  ```bash
  docker build -t tree-detector .
  docker run --gpus all tree-detector --source 0
  ```

- **ONNX / TensorRT / OpenVINO**  
  See [`scripts/export.py`](scripts/export.py) for model conversion.

---

## 🧑‍💻 Contributing

We welcome contributions of all kinds!

- Read our [CONTRIBUTING.md](CONTRIBUTING.md)
- Check open issues or submit a feature request
- See our [Code of Conduct](CODE_OF_CONDUCT.md)

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🌍 Acknowledgments

- [YOLOv11 by ultralytics](https://github.com/ultralytics/ultralytics)
- Open-Source datasets
- Streamlit, Ultralytics

---

## 💬 Community

- GitHub Discussions (coming soon)

---

## ⭐️ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/tree-detector&type=Date)](https://star-history.com/#yourusername/tree-detector)

---
