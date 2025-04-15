# Slide Scrutinizer

![Slide Scrutinizer](https://img.shields.io/badge/Slide-Scrutinizer-4BDFEA?style=for-the-badge)

A powerful web application that analyzes PowerPoint presentations to detect duplicates, calculate content similarities, and check for online presence.

## 🔍 Overview

Slide Scrutinizer is a Flask-based web application designed to help users analyze multiple PowerPoint presentations. It provides a sleek, modern interface with powerful backend functionality to identify duplicate presentations, calculate content similarity between different files, and check for online presence of the content.

## ✨ Features

- **File Upload**: Upload multiple PowerPoint (.pptx) files simultaneously
- **Duplicate Detection**: Automatically identify duplicate presentations using content hashing
- **Content Similarity Analysis**: Calculate and display similarity percentages between presentations
- **Google Presence Check**: Determine if presentation content appears in Google search results
- **Modern UI**: Beautiful, responsive interface with animations and visual feedback
- **Detailed Results**: Clear presentation of analysis results with visual indicators

## 🛠️ Technologies Used

- **Backend**: Python, Flask
- **Frontend**: HTML, CSS, JavaScript
- **PowerPoint Processing**: python-pptx
- **Google Search**: Google Custom Search API
- **Data Storage**: JSON

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.6 or higher
- pip (Python package manager)

## 🚀 Installation & Setup

Follow these steps to get Slide Scrutinizer running on your local machine:

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/slide-scrutinizer.git
   cd slide-scrutinizer
   ```

2. **Create and activate a virtual environment (recommended)**

   ```bash
   # On Windows
   python -m venv venv
   venv\Scripts\activate
   
   # On macOS/Linux
   python -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

   If a requirements.txt file is not included, install the following packages:

   ```bash
   pip install flask python-pptx google-api-python-client werkzeug
   ```

4. **Set up Google Custom Search API (Optional)**

   The application uses Google Custom Search API to check for online presence of content. If you want to use this feature:

   - Create a Google Custom Search Engine at https://cse.google.com/cse/all
   - Get an API key from Google Cloud Console
   - Update the `API_KEY` and `SEARCH_ENGINE_ID` variables in `app.py`

   Note: The application will work without this, but the Google presence check feature will not be functional.

5. **Run the application**

   ```bash
   python app.py
   ```

6. **Access the application**

   Open your web browser and navigate to:
   ```
   http://127.0.0.1:5000/
   ```

## 📊 How to Use

1. **Upload PowerPoint Files**
   - Click the file upload button and select one or more .pptx files
   - Click "Upload & Check" to start the analysis

2. **View Results**
   - **Uploaded PPTs**: List of all uploaded presentations
   - **Skipped PPTs**: Files that couldn't be processed (empty or unreadable)
   - **Duplicate PPTs**: Presentations with identical content
   - **Google Presence**: Percentage indicating how much of the content appears in Google search results
   - **Content Similarity**: Visual representation of similarity between different presentations

## 📁 Project Structure

```
├── app.py                 # Main Flask application
├── templates/             # HTML templates
│   └── index.html         # Main interface template
├── uploads/               # Directory for uploaded files
├── data.json              # Stores analysis results
└── README.md              # Project documentation
```

## 🔒 Privacy & Security

- All uploaded files are stored locally on your machine
- No data is sent to external servers except for Google search queries
- Files can be manually deleted from the `uploads` directory

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [Flask](https://flask.palletsprojects.com/) - The web framework used
- [python-pptx](https://python-pptx.readthedocs.io/) - PowerPoint processing library
- [Google Custom Search API](https://developers.google.com/custom-search/) - For content presence checking

---

<p align="center">Made with ❤️ for PowerPoint analysis</p>