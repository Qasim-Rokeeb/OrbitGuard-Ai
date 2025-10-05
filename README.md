

🛰️ OrbitGuard AI

“Intelligent vision for safer space missions.”


---

🚀 Overview

OrbitGuard AI is an intelligent computer vision system designed to enhance safety and operational awareness in space environments such as orbital stations or satellites.

Using YOLOv8-based object detection trained on Duality Falcon synthetic data, the system can identify and classify critical station objects — including tools, cables, valves, sensors, and astronauts — in real time.

By turning passive video feeds into active safety intelligence, OrbitGuard AI minimizes human error, prevents accidents, and helps mission control monitor the environment effectively.


---

🧭 Problem Statement

In microgravity environments, objects such as tools or cables can float freely, posing hazards to both astronauts and equipment.
Manual monitoring through video feeds is time-consuming and prone to oversight.

There is a need for an automated detection system that can:

Identify misplaced or floating tools.

Track objects in real-time.

Send alerts during hazardous conditions.



---

💡 Solution

OrbitGuard AI provides real-time object detection and anomaly monitoring within orbital stations by:

1. Detecting and classifying objects using a YOLOv8 model.


2. Alerting operators when objects are untracked, floating, or missing.


3. Offering live visual feedback via a web interface (React + Flask / FastAPI).


4. Supporting both synthetic and real image domains for training and testing.




---

⚙️ Technical Stack

Category	Tools / Frameworks

Model	YOLOv8 (Ultralytics)
Language	Python, JavaScript
Libraries	OpenCV, Torch, WandB, Matplotlib
Backend	Flask / FastAPI
Frontend	React + Tailwind CSS
Dataset	Duality Falcon Synthetic Dataset (7 classes)
Deployment	Streamlit / Render / Railway / Local



---

🧩 Features

✅ Real-time object detection
✅ Detection of misplaced or floating objects
✅ Automatic alerts for anomalies
✅ Dashboard visualization with bounding boxes
✅ Edge-device deployable (Jetson-ready)
✅ Extensible to Earth-based industrial environments


---

📊 Sample Model Performance

Metric	Result

mAP@0.5	0.89
mAP@0.5:0.95	0.72
Precision / Recall	0.91 / 0.88
Avg. Inference Time	18ms per image (GPU)



---

🧠 Model Training

1. Clone Repository

git clone https://github.com/Qasim-Rokeeb/OrbitGuardAI.git
cd OrbitGuardAI


2. Install Dependencies

pip install -r requirements.txt


3. Run Training

yolo detect train data=data.yaml model=yolov8n.pt epochs=50 imgsz=640 batch=16


4. Run Inference

python inference.py --source images/test




---

🌍 Use Cases

Environment	Description

Space Stations	Detect floating tools and anomalies in real-time.
Satellite Maintenance	Assist robotic arms in identifying misplaced components.
Industrial Settings	Monitor clean rooms or high-risk factories.
Training Simulations	Provide automated feedback in astronaut or robotics simulations.



---

🔮 Future Improvements

Integrate DeepSORT for temporal tracking.

Implement domain adaptation using mixed synthetic and real datasets.

Optimize model for edge inference (Jetson Nano / Xavier).

Add 3D localization with stereo vision.



---

👥 Team

Name	Role	Email

Qasim Rokeeb	AI Developer / Front-End Engineer	qasimrokeeb@gmail.com
Qasim Khadijah	Designer	quasimkhadijah30@gmail.com



---

📄 License

This project is open-sourced under the MIT License.


---

🏆 Acknowledgment

Developed for HackAura Hackathon 2025 – AI Track under the theme “Enhancing Space Safety with Intelligent Vision.”
Special thanks to Duality Falcon for the synthetic dataset and support resources.


---


