
# 🖱️ Eye-Controlled Mouse

This project uses a webcam to control the mouse cursor using eye movement and blink detection. It leverages **MediaPipe Face Mesh** for facial landmark detection and **PyAutoGUI** to control the system mouse.

## 🚀 Features

* Cursor movement using eye position
* Left click triggered by blinking (using eye landmarks)
* Real-time performance (optimized with buffer settings)

---

## 🧰 Technologies Used

* Python 3
* OpenCV (`cv2`)
* MediaPipe (`mediapipe`)
* PyAutoGUI (`pyautogui`)

---

## 🛠️ Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/eye-control-mouse.git
   cd eye-control-mouse
   ```

2. **Install required packages:**

   ```bash
   pip install opencv-python mediapipe pyautogui
   ```

---

## ▶️ Usage

1. **Run the script:**

   ```bash
   python eye_mouse.py
   ```

2. **Instructions:**

   * Use your **right eye** to move the cursor.
   * **Blink your left eye** to simulate a mouse click.
   * Press `ESC` to exit the application.

---

## ⚙️ How It Works

* MediaPipe Face Mesh detects **facial landmarks**.
* Landmarks around the right eye are used to move the mouse:

  * Specifically, points `474–477` are used.
* Left eye blink is detected using vertical distance between landmarks `145` and `159`. If the distance drops below a threshold, a click is triggered.
* Frame is flipped horizontally to ensure mirror-like interaction.

---

Link -https://www.youtube.com/watch?v=cEGwnMckWjw


## 🧠 Future Enhancements

* Add right-click via right eye blink
* Add drag functionality
* Improve blink detection threshold using adaptive methods
* GUI to calibrate sensitivity


## 📄 License

This project is open-source under the MIT License.

