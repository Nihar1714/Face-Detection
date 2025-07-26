# Face Detection & Attendance System

This project is a **face recognition-based attendance system** built using **Python**, **Tkinter**, **OpenCV**, and **facenet-pytorch**.  
It allows user registration, face detection, recognition, and automatic attendance marking with late arrival tracking.

## Features
- **Face Registration:** Capture user faces and store embeddings.
- **Face Recognition:** Match live faces with registered users.
- **Attendance Management:**
  - Marks attendance with date and time.
  - Identifies **On-time** or **Late** arrivals based on a configurable start time.
- **Admin Panel:**
  - View attendance records.
  - Export attendance data to Excel.
- **GUI Interface:** Built using Tkinter with real-time camera feed.

## Requirements
Install the following Python libraries:
```bash
pip install torch facenet-pytorch opencv-python numpy pandas pillow tk
```

## File Structure
```
face_detection.ipynb
face_database/          # Stores registered faces and embeddings (.jpg, .npy)
attendance.xlsx         # Stores attendance logs
```

## How to Run
1. **Ensure Python 3.8+ is installed.**
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook or convert it to a Python script:
   ```bash
   jupyter notebook face_detection.ipynb
   ```
   or
   ```bash
   python face_detection.py
   ```
4. **Register Users:**
   - Click "Register User" → Enter a User ID → Capture face.
5. **Mark Attendance:**
   - Click "Mark Attendance" → System recognizes user → Attendance is recorded.
6. **Admin Panel:**
   - Click "Admin Panel" → Enter credentials → View/Export attendance.

## Default Admin Credentials
- **Username:** `admin`
- **Password:** `admin123`

> *For production, do not hardcode credentials. Use secure storage.*

## Notes
- Ensure your webcam is accessible.
- For accurate recognition:
  - Only one person should be in the frame.
  - Register in good lighting.
- Modify `work_start_time` in code to adjust late arrival threshold.

