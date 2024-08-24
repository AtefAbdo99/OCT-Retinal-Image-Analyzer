# OCT Retinal Image Analyzer

OCT Retinal Image Analyzer is a web application that allows medical professionals and researchers to upload and classify Optical Coherence Tomography (OCT) retinal images. The app uses a pre-trained deep learning model to provide accurate predictions and confidence scores for common retinal conditions such as CNV, DME, DRUSEN, and NORMAL.

The application also provides statistical insights based on previous classifications, including class distribution, mean age of patients, mean model accuracy, and the most common diagnosis.

## Features

- **Image Upload and Classification:** Upload an OCT retinal image and receive a classification prediction with a confidence score.
- **Historical Data:** View all previous classifications with detailed information about the patient and the image.
- **Statistical Insights:** Get detailed statistics including class distribution, mean age, mean accuracy, total images processed, and most common diagnosis.
- **Responsive Design:** The app uses modern frontend frameworks (Vue.js, Tailwind CSS) for a responsive and user-friendly experience.
- **Scalable Backend:** Built with Flask and SQLAlchemy, the app stores all classification data in a SQLite database.

## Demo

![OCT Retinal Image Analyzer Demo](path_to_your_demo_image_or_gif)

## Installation

### Prerequisites

- Python 3.7+
- TensorFlow 2.x
- Flask
- SQLite

### Clone the Repository

```bash
git clone https://github.com/your_username/OCT-Retinal-Image-Analyzer.git
cd OCT-Retinal-Image-Analyzer

etup Python Environment
It's recommended to create a virtual environment:

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install Dependencies
bash
Copy code
pip install -r requirements.txt
Download the Model
Ensure you have the pre-trained model oct_classification_final_model_lg.keras in the root directory of the project. You can download it from Google Drive or train your own model.

Database Setup
The app uses SQLite for storing classification history. The database will be automatically created when you run the app for the first time.

Run the Application
bash
Copy code
flask run
Visit http://127.0.0.1:5000 in your browser to access the app.

API Endpoints
/api/classify [POST]: Upload an OCT image and receive a classification prediction.
/api/history [GET]: Retrieve the full history of all classifications made by the app.
/api/statistics [GET]: Retrieve statistical data, including class distribution, mean age, mean accuracy, and most common diagnosis.
Frontend
The frontend is built using:

Vue.js for interactive UI components.
Tailwind CSS for modern styling.
Chart.js for visualizing statistical data.
Backend
The backend is powered by:

Flask for handling requests and responses.
TensorFlow for loading and running the trained deep learning model.
SQLAlchemy for managing the SQLite database.
Deployment
For deployment, you can use services like Heroku, AWS, or Google Cloud. Ensure that the required environment variables and model files are properly configured.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
We welcome contributions to improve the OCT Retinal Image Analyzer. Feel free to submit a pull request or create an issue for any bugs or feature requests.

Contact
If you have any questions or need further assistance, please contact:

Author: Atef Hassan
Email: your_email@example.com
yaml
Copy code

---

### `.gitignore`:

Add the following lines to your `.gitignore` file to prevent sensitive or unnecessary files from being committed to the repository:

```gitignore
# Python
*.pyc
__pycache__/
venv/

# Flask and SQLAlchemy
instance/
*.sqlite3
oct_classifications.db

# TensorFlow model
*.h5
*.keras

# Uploads
static/uploads/
Additional Files:
requirements.txt: List all the required dependencies for the project, such as:

plaintext
Copy code
Flask
Flask-SQLAlchemy
Flask-Cors
TensorFlow
numpy
Pillow
LICENSE: Consider adding an MIT license file to the repository for open-source usage.

By following this template, you'll create a well-structured GitHub repository for your OCT Retinal Image Analyzer project, making it easy for others to understand, use, and contribute to your project.

