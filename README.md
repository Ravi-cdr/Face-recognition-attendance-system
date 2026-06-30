# Face Recognition Attendance System

A real-time, automated attendance system built in Python that uses facial recognition to mark student/employee attendance through a live webcam feed — eliminating manual roll calls and proxy attendance.

## Abstract

Manual attendance tracking is time-consuming and prone to errors and proxy marking. This project solves that problem using computer vision: it detects and recognizes faces in real time through a webcam, matches them against a database of known faces, and automatically logs attendance with date and time. Face detection and recognition are handled using OpenCV and the `face_recognition` (dlib-based) library, with attendance records stored securely in an SQLite database.

## Features

- Real-time face detection and recognition via webcam
- Automatic attendance marking with timestamp (no manual entry)
- Prevents duplicate attendance entries for the same person on the same day
- Simple desktop GUI built with Tkinter
- Attendance records stored and retrieved using SQLite
- Easily extendable to add new faces/students to the system

## Tech Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Face Detection & Recognition | OpenCV, dlib, face_recognition |
| Numerical Processing | NumPy |
| GUI | Tkinter |
| Database | SQLite |

## Project Structure

| File | Description |
|---|---|
| `main.py` | Entry point — launches the application |
| `AttendanceProject.py` | Core face detection and recognition logic |
| `attendance.py` | Handles attendance marking and logging |
| `AttRecords.py` | Manages reading/writing attendance records |
| `NameMapping.csv` | Maps detected face IDs to student/employee names |
| `Images_Attendance.zip` | Reference face images used for recognition |
| `attendance.db` | SQLite database storing attendance logs |

## How to Run

1. Clone this repository
2. git clone https://github.com/<your-usernam>/face-recognition-attendance-system.git
cd face-recognition-attendance-system

2. Install dependencies
pip install -r requirements.txt

3. Add reference face images to the images folder (extract `Images_Attendance.zip`)

4. Run the application
python main.py

5. The webcam will open and start detecting faces. Recognized faces are automatically marked present in the database.

## Future Improvements

- Add a login/admin panel to manage registered users
- Export attendance reports to Excel/PDF
- Add email/SMS notification on attendance marking
- Deploy as a web app using Flask

## Author

**Ravi Kumar**
BCA Graduate, CIMAGE Professional College, Patna
