# ShrinkIt: A Comprehensive File Utility Web Application

ShrinkIt is a full-stack web application designed to streamline common file manipulation tasks, offering robust capabilities for compression, type conversion, and image editing through an intuitive user interface.

## Features

* **Intelligent File Compression:** Reduce file sizes for various formats (images, text, documents) with options for automatic optimization or user-specified compression levels (e.g., quality percentage for images). Leverages `zlib` and `Pillow` for actual compression.
* **Versatile File Type Conversion:** Convert between a wide range of formats, including:
    * Image to PDF & PDF to Image (JPG, PNG)
    * Image to Image (JPG, PNG, WEBP, GIF)
    * TXT to PDF
    * XLSX to CSV & CSV to XLSX
    * CSV to PDF (rendered as a table)
* **Comprehensive Image Editing Suite:** Apply common image transformations directly:
    * **Resizing:** Adjust image dimensions to exact pixel values.
    * **Cropping:** Define and apply custom crop areas.
    * **Rotation:** Rotate images by arbitrary degrees or quick 90-degree increments (left/right).
    * **Flipping:** Mirror images horizontally or vertically.
    * **Filters:** Enhance images with grayscale, sepia tone, blur, and sharpen effects.
* **File Management:** Easily download processed files and delete files from the server.
* **Responsive & User-Friendly UI:** Built with Tailwind CSS to ensure optimal viewing and usability across all devices (mobile, tablet, desktop), featuring clear feedback messages.

## Technologies Used

* **Backend:** Python, Flask, Flask-CORS, Pillow, PyMuPDF, openpyxl, ReportLab
* **Frontend:** HTML5, CSS3 (Tailwind CSS), JavaScript

## Setup and Running Locally

To get ShrinkIt running on your local machine, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/ShrinkIt-File-Utility.git](https://github.com/your-username/ShrinkIt-File-Utility.git)
    cd ShrinkIt-File-Utility
    ```
    (Replace `your-username/ShrinkIt-File-Utility` with your actual repository path)

2.  **Install Python:**
    Ensure you have Python (3.7+ recommended) installed. You can download it from [python.org](https://www.python.org/downloads/).

3.  **Install Dependencies:**
    It's highly recommended to use a [Python virtual environment](https://docs.python.org/3/library/venv.html) to manage dependencies.
    ```bash
    # Create a virtual environment (optional but recommended)
    python -m venv venv
    # Activate the virtual environment
    # On Windows: .\venv\Scripts\activate
    # On macOS/Linux: source venv/bin/activate

    # Install required Python libraries
    pip install -r requirements.txt
    ```
    *If you encounter `ModuleNotFoundError: No module named 'pip'` during `pip install`, first try to repair pip:*
    `python -m ensurepip --default-pip`
    *If you have multiple Python installations and issues persist, use the full path to your desired `python.exe` for all commands (e.g., `"C:\Path\To\Python313\python.exe" -m pip install -r requirements.txt`).*

4.  **Run the Backend Server:**
    In your terminal (with the virtual environment activated, if used), start the Flask backend:
    ```bash
    python app.py
    ```
    Keep this terminal window open; the server must be running for the frontend to function. You should see "File Utility Backend is running!" in your browser if you navigate to `http://127.0.0.1:5000/`.

5.  **Open the Frontend:**
    Locate the `index.html` file in your `ShrinkIt-File-Utility` folder. Double-click it or open it with your preferred web browser.

## Stopping the Tool

To stop the backend server, go to the terminal/command prompt window where it's running and press `Ctrl + C`.

---
