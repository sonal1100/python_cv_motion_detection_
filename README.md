# Real-Time Motion Detection using Python & OpenCV

## Objective
The goal of this project is to detect motion from a webcam in real time using Python and OpenCV.  
Detected motion events are saved in an SQLite database for later verification.


## Technologies Used
- Python
- OpenCV
- SQLite
- Time module



## How It Works
1. The webcam captures live video frames.
2. Each frame is converted to grayscale and blurred for easier processing.
3. Motion is detected by comparing the current frame with the previous frame.
4. If enough pixels change (motion detected), an event is created.
5. Events include:
   - Timestamp
   - Event type (`motion_detected`)
   - Number of pixels changed
6. Events are stored in a local SQLite database.
7. The program runs for a limited number of frames (150) in Jupyter Notebook.
8. Database contents can be verified using a SELECT query.



## Image Processing Technique Used
- **Grayscale conversion**: Converts the frame to grayscale to simplify processing.
- **Gaussian blur**: Reduces noise in the frame.
- **Frame differencing**: Detects motion by calculating differences between consecutive frames.
- **Thresholding**: Highlights areas with significant changes.



## How to Run
1. Make sure Python and required libraries are installed:
```bash
pip install opencv-python
Open Motion_Detection_Assignment.ipynb in Jupyter Notebook.

Run the cells in order:

Cell 1: Imports
Cell 2: MotionDetector class
Cell 3: Database functions
Cell 4: Main motion detection loop
Cell 5: Database verification (optional)
The program prints motion events in the notebook and stores them in events.db.

## Screenshots

### Motion Detection Output
Motion detected events("C:\Users\SONAL NIKAM\OneDrive\Desktop\md\motion_events.png")

### Stored Events in Database
Database events("C:\Users\SONAL NIKAM\OneDrive\Desktop\md\database_eventss.png")

