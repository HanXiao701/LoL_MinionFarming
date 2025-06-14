# LoL_MinionFarming
# LoL Minion Action Analysis Toolkit

This repository contains code and data used in the thesis project analyzing player behavior and cognitive metrics in the laning phase of *League of Legends*. The project focuses on extracting minion farming performance indicators from gameplay videos and Riot API data, with an emphasis on computer vision-based analysis.

---

## 🔍 Project Overview
The goal of this project is to evaluate how players manage minion waves using vision-based metrics, and how these measures correlate with in-game performance data obtained via the Riot API. Core indicators include:

- **CS@10** and **Gold@10** estimation from video
- **Skill Execution Ratio (SER)** and **Wave Efficiency**
- **Minion type inference** via reverse mapping from gold gain
- **Cross-validation** against API data for different ranks and matchups

This project includes code for:
- Video frame extraction and processing
- Minion event tracking using YOLOv8 (experimental)
- Riot API data integration and matchup analysis
- Metric computation and visualization

---

## 📁 Directory Structure
```
LoL_minionAction/
├── videos/                         # Raw video files
├── yolo_dataset/                  # YOLO training/validation data
├── data_analysis/                # Example processed Riot API and video comparison data analysis code
├── model/                         # Placeholder for saved models
├── runs/                          # YOLOv8 training logs and checkpoints
├── YOLO_detect.ipynb             # YOLOv8 inference notebook
├── YOLO_train.ipynb              # YOLOv8 training script (not finalized)
├── YOLO_video_process.ipynb      # YOLO-based frame annotation
├── analyze_matchup.ipynb         # Matchup-level analysis script
├── data_collection.ipynb         # Riot API data collection
├── video_process.ipynb           # Frame extraction and video handling
├── video_analyze.ipynb           # Compute SER, CS@10, wave efficiency
└── README.md                     # This file
```

---

## ⚠️ YOLOv8 Usage Notice
This project includes experimental usage of YOLOv8 (`yolov8n.pt`) for minion detection. Due to limited training data and noisy annotations, the accuracy was insufficient for reliable quantitative use. As such, **YOLO-based methods are not used in the thesis’s final reported results**. They are included here as exploratory work and for potential future improvements.

---

## 📦 Requirements
- Python 3.9+
- OpenCV
- pandas
- seaborn / matplotlib
- ultralytics (for YOLOv8)

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run
1. Collect gameplay videos into the `videos/` folder.
2. Run `video_process.ipynb` to extract frames.
3. (Optional) Run YOLO detection via `YOLO_detect.ipynb`.
4. Run `analyze_matchup.ipynb` to extract metrics like SER and efficiency.
5. Load Riot API data using `data_collection.ipynb`. Please replace the API key accordingly.
6. Use `video_data_analysis/` notebooks to compare video and API data.

---

## 📊 Outputs
- LaTeX tables and plots for thesis presentation
- Frame-level minion tracking logs
- Peer performance comparisons

---

## 🧠 Thesis Integration
This code supports the methodology and results chapters of the thesis project on cognitive load and strategy in *League of Legends*. Metrics like **Skill Execution Ratio** and **Wave Efficiency** were shown to correlate with rank and playstyle based on both video data and Riot API.

For more details, please refer to the final thesis document.

---

## 📫 Contact
This project was developed as part of a Master's thesis at Eindhoven University of Technology. For academic inquiries or collaboration, please contact [Your Name / Email Here].
# LoL Minion Action Analysis Toolkit

This repository contains code and data used in the thesis project analyzing player behavior and cognitive metrics in the laning phase of *League of Legends*. The project focuses on extracting minion farming performance indicators from gameplay videos and Riot API data, with an emphasis on computer vision-based analysis.

---

## 🔍 Project Overview
The goal of this project is to evaluate how players manage minion waves using vision-based metrics, and how these measures correlate with in-game performance data obtained via the Riot API. Core indicators include:

- **CS@10** and **Gold@10** estimation from video
- **Skill Execution Ratio (SER)** and **Wave Efficiency**
- **Minion type inference** via reverse mapping from gold gain
- **Cross-validation** against API data for different ranks and matchups

This project includes code for:
- Video frame extraction and processing
- Minion event tracking using YOLOv8 (experimental)
- Riot API data integration and matchup analysis
- Metric computation and visualization

---

## 📁 Directory Structure
```
LoL_minionAction/
├── videos/                         # Raw video files
├── yolo_dataset/                  # YOLO training/validation data
├── yolo_extracted_frames/        # YOLO-specific frames for detection
├── extracted_frames_MM/          # Frames from Melee vs Melee (MM) matchups
├── extracted_frames_MR/          # Frames from Melee vs Ranged (MR)
├── extracted_frames_RM/          # Frames from Ranged vs Melee (RM)
├── extracted_frames_RR/          # Frames from Ranged vs Ranged (RR)
├── data_analysis/                # Processed Riot API and video comparison code
├── video_data_analysis/          # Final scripts to correlate metrics
├── model/                         # Placeholder for saved models
├── runs/                          # YOLOv8 training logs and checkpoints
├── YOLO_detect.ipynb             # YOLOv8 inference notebook
├── YOLO_train.ipynb              # YOLOv8 training script (not finalized)
├── YOLO_video_process.ipynb      # YOLO-based frame annotation
├── analyze_matchup.ipynb         # Matchup-level analysis script
├── data_collection.ipynb         # Riot API data collection
├── video_process.ipynb           # Frame extraction and video handling
├── video_analyze.ipynb           # Compute SER, CS@10, wave efficiency
├── performance_comparison_report.csv   # Peer comparison data
├── quantitative_results.csv              # Final metric summaries
└── README.md                     # This file
```

---

## ⚠️ YOLOv8 Usage Notice
This project includes experimental usage of YOLOv8 (`yolov8n.pt`) for minion detection. Due to limited training data and noisy annotations, the accuracy was insufficient for reliable quantitative use. As such, **YOLO-based methods are not used in the thesis’s final reported results**. They are included here as exploratory work and for potential future improvements.

---

## 📦 Requirements
- Python 3.9+
- OpenCV
- pandas
- seaborn / matplotlib
- ultralytics (for YOLOv8)

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run
1. Collect gameplay videos into the `videos/` folder.
2. Run `video_process.ipynb` to extract frames.
3. (Optional) Run YOLO detection via `YOLO_detect.ipynb`.
4. Run `analyze_matchup.ipynb` to extract metrics like SER and efficiency.
5. Load Riot API data using `data_collection.ipynb`. Please replace the API key accordingly.
6. Use `video_data_analysis/` notebooks to compare video and API data.

---

## 📊 Outputs
- LaTeX tables and plots for thesis presentation
- Frame-level minion tracking logs
- Peer performance comparisons

---

## 🧠 Thesis Integration
This code supports the methodology and results chapters of the thesis project on cognitive load and strategy in *League of Legends*. Metrics like **Skill Execution Ratio** and **Wave Efficiency** were shown to correlate with rank and playstyle based on both video data and Riot API.

For more details, please refer to the final thesis document.

---

## 📫 Contact
This project was developed as part of a Master's thesis at Eindhoven University of Technology. For academic inquiries or collaboration, please contact [Your Name / Email Here].
