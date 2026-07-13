# AttendanceMonitoringSystem

# Attendance Monitoring System

A Python-based Face Recognition Attendance Monitoring System that automates attendance recording using computer vision and facial recognition. The application captures student faces, trains a recognition model, identifies students in real time through a webcam, and stores attendance records automatically.

---

## Features

- Register new students with facial images
- Train the facial recognition model
- Real-time face recognition using webcam
- Automatic attendance recording
- Stores attendance records in CSV format
- Simple desktop GUI built with Tkinter
- Uses OpenCV Haar Cascade for face detection
- Easy student management

---

## Tech Stack

- Python 3
- OpenCV
- Tkinter
- NumPy
- Pandas
- Pillow (PIL)
- OpenCV Face Recognition (LBPH)
- Haar Cascade Classifier

---

## Project Structure

```
AttendanceMonitoringSystem/
│
├── Attendance/                 # Generated attendance CSV files
├── StudentDetails/             # Student information
├── TrainingImage/              # Student face images
├── TrainingImageLabel/         # Trained face recognition model
├── haarcascade_frontalface_default.xml
├── main.py                     # Main application
├── requirements.txt
├── README.md
└── SPECIFICATIONS_OF_THIS_PROJECT.txt
```

---

## How It Works

### 1. Register Student

- Enter Student ID
- Enter Student Name
- Capture multiple face images using the webcam
- Images are stored inside the `TrainingImage` directory.

### 2. Train Model

The application processes all captured images and trains an LBPH (Local Binary Patterns Histogram) face recognition model.

The trained model is saved inside:

```
TrainingImageLabel/
```

### 3. Take Attendance

- Opens the webcam
- Detects faces in real time
- Recognizes registered students
- Automatically records:
  - Student ID
  - Student Name
  - Date
  - Time

Attendance is saved in:

```
Attendance/
```

---

## Installation

### Clone the repository

```bash
git clone https://github.com/Dexturn1/AttendanceMonitoringSystem.git

cd AttendanceMonitoringSystem
```

### Create Virtual Environment (Optional)

Windows

```bash
python -m venv venv

venv\Scripts\activate
```

macOS/Linux

```bash
python3 -m venv venv

source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Application

```bash
python main.py
```

---

## Requirements

Python 3.8 or later

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Dependencies

- opencv-python
- opencv-contrib-python
- numpy
- pandas
- pillow

---

## Dataset

Captured facial images are stored inside:

```
TrainingImage/
```

Each registered student has their own training images which are used for model training.

---

## Attendance Output

Attendance records are automatically generated as CSV files.

Example:

```
Attendance/

Attendance_13-07-2026.csv
```

Each file contains:

| Student ID | Name | Date | Time |
| ---------- | ---- | ---- | ---- |

---

## Face Recognition Pipeline

```
Student Registration
          │
          ▼
Capture Face Images
          │
          ▼
Train LBPH Model
          │
          ▼
Open Webcam
          │
          ▼
Detect Faces
          │
          ▼
Recognize Student
          │
          ▼
Record Attendance
          │
          ▼
Save CSV File
```

---

## Future Improvements

- Database integration (MySQL/PostgreSQL)
- Cloud attendance synchronization
- Flask/Django web dashboard
- Email attendance reports
- Admin login system
- Deep learning face recognition (FaceNet / ArcFace)
- Live analytics dashboard
- Student profile management
- Multi-camera support

---

## Known Limitations

- Performance depends on image quality and lighting conditions.
- Requires sufficient training images for reliable recognition.
- Current attendance storage uses CSV files instead of a database.
- Designed primarily for classroom-sized deployments.

---

## Contributing

Contributions are welcome.

If you would like to improve the project:

1. Fork the repository
2. Create a new feature branch

```bash
git checkout -b feature/YourFeature
```

3. Commit your changes

```bash
git commit -m "Add new feature"
```

4. Push the branch

```bash
git push origin feature/YourFeature
```

5. Open a Pull Request.

---

## License

This project is open source and available under the MIT License.

---

## Author

**Prabhat Kapkoti**

GitHub: https://github.com/Dexturn1
