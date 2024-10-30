# Blum Airdrop Clicker Bot

This Python script automates mouse clicking for the Blum Airdrop Bot. It identifies specific color regions on the screen and clicks on them automatically, streamlining the repetitive clicking tasks associated with airdrop processes.

## Preview

![Preview](https://github.com/user-attachments/assets/c5c9cdb3-82e0-452b-bb4f-50c25ef01d0b)

## Features

- **Automated Mouse Clicking**: Automatically clicks on a target color that you specify.
- **Customizable Region**: Adjust the screen region that the program monitors for clicks.
- **Start/Stop Control**: Use keyboard keys to start (`s`) and stop (`p`) the clicking process.
- **Screen Compatibility**: The default region is set for 1080p resolution but can be modified for different screen sizes.

## Prerequisites

Before running this program, ensure you have the following libraries installed:

- `opencv-python`
- `numpy`
- `pyautogui`
- `pynput`

You can install them using pip:

```bash
pip install opencv-python numpy pyautogui pynput
```

## How to Use

1. **Clone the repository** or download the Python script:

   ```bash
   git clone https://github.com/yourusername/Blum-Airdrop-Clicker.git
   ```

2. **Edit the region settings** (if necessary):

   The default screen region is set for a 1080p resolution. If your screen has a different resolution, update the `region` variable inside the script:

   ```python
   region = (720, 155, 475, 620)
   ```

   Adjust the `region` values according to your screen size:
   - `(x, y, width, height)` corresponds to the top-left corner of the region and the size of the area to be monitored for clicks.

3. **Run the program**:

   Execute the Python script:

   ```bash
   python Blum_Airdrop_Clicker.py
   ```

4. **Start and Stop Clicking**:

   - Press the `s` key to start auto-clicking.
   - Press the `p` key to stop auto-clicking.
   - Press the `q` key to quit the program.

## Customization

- **Color Detection**: Change the `hex_color` variable to target a different color for clicking:

  ```python
  hex_color = "#86817e"  # Replace with your desired hex color
  ```

- **Threshold and Contour Area**: Adjust the `threshold`, `min_area`, and `max_area` variables to fine-tune the color detection sensitivity and the size of areas to click on:

  ```python
  threshold = 10  # Adjust sensitivity
  min_area = 0  # Minimum contour area to consider
  max_area = 1000000000  # Maximum contour area to consider
  ```

## Notes

- Ensure the airdrop window is visible on your screen within the specified region.
- Use caution when using automated clicking scripts to avoid unintentional actions or violations of terms of service.
