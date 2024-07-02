# Image-Similarity-Detection-with-Flask
This repository contains a Flask application for detecting the similarity between two uploaded images. The application processes the images, converts them into vector forms, and calculates their Jaccard similarity score using MinHash.


Overview
This repository contains a Flask application for detecting the similarity between two uploaded images. The application processes the images, converts them into vector forms, and calculates their Jaccard similarity score using MinHash.

Features
Image Upload: Accepts two images for comparison via a web interface.
Image Preprocessing: Resizes, converts to grayscale, and applies Gaussian blur.
Vector Conversion: Converts preprocessed images into vectors.
Similarity Calculation: Uses MinHash to compute the Jaccard similarity score.
API Response: Returns the similarity score in JSON format.
Getting Started
Prerequisites
Ensure you have Python 3.8 or higher installed. You'll need the following Python packages:

Flask
NumPy
OpenCV-Python
datasketch
You can install these packages using pip:

sh
Copy code
pip install Flask numpy opencv-python datasketch
Installation
Clone the Repository

sh
Copy code
git clone https://github.com/yourusername/image-similarity-flask.git
cd image-similarity-flask
Install Dependencies

sh
Copy code
pip install -r requirements.txt
Prepare HTML Templates

Ensure index1.html is placed in the templates directory.

Usage
Run the Flask Application

sh
Copy code
python app.py
Access the Web Interface

Open your web browser and go to http://127.0.0.1:5000/.

Upload Images

Upload two images and click the submit button to get the similarity score.

API Endpoints
GET /
Description: Renders the home page for uploading images.
Response: HTML page with image upload form.
POST /upload
Description: Handles image uploads and calculates similarity.
Request: Expects two image files (img1 and img2) in the form-data.
Response: JSON containing the similarity score.
Example Request
sh
Copy code
curl -F "img1=@path/to/image1.jpg" -F "img2=@path/to/image2.jpg" http://127.0.0.1:5000/upload
Example Response
json
Copy code
{
  "similarity": 0.85
}
Example
Here's an example of how to use the Flask application for image similarity detection:

Access Home Page


Upload Images


View Similarity Score


File Structure
arduino
Copy code

image-similarity-flask/
│
├── templates/
│   └── index1.html
├── images/
│   ├── home_page.png
│   ├── upload_images.png
│   └── similarity_score.png
├── app.py
├── requirements.txt
└── README.md

app.py: Main Flask application script.
requirements.txt: List of dependencies for the project.
README.md: This README file.
Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any features or bug fixes.

Fork the repository.
Create a new branch: git checkout -b feature-branch-name.
Make your changes and commit them: git commit -m 'Add new feature'.
Push to the branch: git push origin feature-branch-name.
Submit a pull request.
