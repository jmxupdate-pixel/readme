# OpenCV Feature Matching & Rotation Detection

This project uses **OpenCV** to detect features between two images, match them, and visualize the matches.
It works in **headless environments** (Linux servers, SSH, Colab) by saving outputs to files instead of opening GUI windows.

---

## 📦 Requirements

Python 3.7+

```bash
sudo apt update
sudo apt install python3 python3-pip
```

Install dependencies:

```bash
pip install opencv-python-headless matplotlib numpy
```

---

## 📂 Project Structure

```
.
├── match_rotation.py       # Main script
├── reference.jpg           # First image
├── rotated.jpg             # Second image (can be rotated)
├── README.md
```

---

## ▶️ Usage

Run:

```bash
python3 match_rotation.py reference.jpg rotated.jpg
```

Outputs:

```
reference_keypoints.jpg    # Keypoints detected in first image
rotated_keypoints.jpg      # Keypoints detected in second image
matches.jpg                # Matches between both images
matches_plot.png           # Matplotlib version of matches
```

---

## 🛠 Notes

* If you **want GUI popups** instead of saving to files:

  ```bash
  sudo apt install libgtk2.0-dev pkg-config
  pip uninstall opencv-python-headless
  pip install opencv-python
  ```
* To increase accuracy, edit `match_rotation.py`:

  ```python
  orb = cv2.ORB_create(nfeatures=2000)
  ```
* You can also switch to SIFT:

  ```python
  sift = cv2.SIFT_create()
  ```

---

## 📜 License

MIT
