# Browser-Based PDF Merger

A simple, client-side web application for merging multiple PDF files into one. Many times I needed to create a merged PDF for official work but did not feel comfortable uploading sensitive files to third-party websites. This tool allows PDFs to be merged entirely in the browser, so your files remain private and never leave your device.

## ✨ Features

* **Client-Side Processing**: All file merging happens locally in your browser. PDFs are never uploaded to a server, ensuring your data remains private and secure.
* **Lightweight Deployment**: The application is a static site, consisting of only HTML, CSS, and JavaScript, making it extremely fast and easy to deploy.
* **Powered by Pyodide**: The core logic is a Python script that runs within the browser's sandbox using the **Pyodide** framework, which ports the CPython interpreter to WebAssembly.

## 🛠️ How It Works

The magic behind this project is the combination of a few key technologies:

1.  **HTML**: Provides the user interface, including the file input and merge button.
2.  **JavaScript**: Manages the user interaction, loads the Pyodide environment, and handles the file transfer between the user's local machine and the Python script running in the browser.
3.  **Pyodide**: Runs a Python script that uses the **`pypdf`** library to merge the PDFs. The script operates on a virtual file system created by Pyodide, where the selected files are temporarily stored.
4.  **CSS**: Styles the interface to provide a clean and user-friendly experience.


**Live Demo:** Try it [here](https://vab-jain.github.io/pdf-merger-website/).
