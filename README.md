# introducing Blacino personal cooking assistant with Advanced AI Features

  Introducing Blacino – the smart recipe provider that transforms your cooking experience. Powered by cutting-edge AI, Blacino offers personalized recipe recommendations, ingredient recognition, and intelligent tagging. Using advanced models like LangChain, TensorFlow, PyTorch, and YOLOv5, it processes real-time images and live video to identify ingredients and suggest recipes based on your preferences. With Blacino, cooking becomes simpler, smarter, and more enjoyable.

![IMG_20241222_024433](https://github.com/user-attachments/assets/3355e327-a9b6-4527-810f-ffbf3ab1584b)
*Developed by Sandip.*

## Overview

Blacino is designed to make recipe discovery simple and personalized. By combining a user-friendly interface with powerful artificial intelligence technology, it offers a seamless cooking experience. Users can:

Upload images of ingredients or dishes: Using YOLOv5, Blacino performs real-time ingredient detection, instantly recognizing items in your kitchen.

Receive personalized recipe suggestions: Based on the detected ingredients and your dietary preferences, Blacino uses LangChain’s artificial intelligence recommendation engine to provide tailored recipe ideas.

Benefit from intelligent recipe tagging: Recipes are automatically categorized (e.g., vegan, gluten-free, low-carb) based on ingredient recognition and nutritional analysis, making it easier to find what fits your needs.

Enjoy an interactive experience: Built with React, Blacino offers smooth navigation, real-time updates, and a user-friendly interface that enhances your cooking journey.




## Key Features

- **AI-Powered Recipe Recommendations:** LangChain's AI model analyzes user preferences and suggests recipes tailored to dietary restrictions, past choices, and ingredient availability.
- **Ingredient Recognition via YOLOv5:** Upload images of food or ingredients, and the app uses YOLOv5's object detection to identify items in the image, such as vegetables, fruits, meats, and more.
- **Smart Recipe Tagging & Filtering:** Recipes are automatically tagged based on detected ingredients (e.g., "vegan," "high-protein," "low-carb"), allowing users to filter recipes according to their dietary needs.
- **Advanced Image Processing:** TensorFlow and PyTorch are used for deeper analysis of the ingredients, such as categorizing them into broader food groups (e.g., dairy, grains) and estimating nutritional content.
- **Interactive UI Built with React:** A responsive, modern interface that allows users to easily interact with the application, upload images, browse recipes, and view suggestions.

## Technologies Used

- **Frontend:** React (JavaScript), HTML5, CSS3, Axios for API calls
- **Backend:** Python (Flask, FastAPI, or Django), TensorFlow, PyTorch, YOLOv5, LangChain
- **AI Models:**
  - **LangChain:** Provides AI-driven, personalized recipe suggestions by analyzing user preferences and available ingredients.
  - **YOLOv5 (You Only Look Once):** Detects and identifies ingredients in images in real-time.
  - **TensorFlow/PyTorch:** Used for image classification, ingredient categorization, and nutritional analysis.
- **Database:** MongoDB or PostgreSQL for storing recipes, user data, and AI-generated recommendations.
- **API Communication:** RESTful API for seamless interaction between the frontend and backend.

## How It Works

The application integrates various AI models into a complex but efficient pipeline. Here's how the main components interact:

1. **User Interaction (Frontend):** The user uploads an image of ingredients or dishes through the React-based frontend.
2. **Image Processing (Backend):** The backend uses YOLOv5 to perform object detection on the uploaded image, identifying the ingredients.
3. **Ingredient Analysis (TensorFlow/PyTorch):** After detecting the ingredients, TensorFlow or PyTorch models analyze them for further categorization (e.g., vegetables, dairy, protein) and nutritional insights.
4. **Personalized Recommendation (LangChain):** Based on the ingredients detected and the user's preferences, LangChain generates personalized recipe recommendations, taking into account dietary restrictions, cuisine types, and previous interactions.
5. **Smart Recipe Tagging:** Recipes are tagged with categories based on the recognized ingredients, making it easier for users to filter and find recipes that meet their needs (e.g., "low-calorie," "vegan," "gluten-free").

## Setting Up the Project

### Prerequisites

Ensure the following tools are installed on your system:

- [Node.js](https://nodejs.org/) (for React frontend)
- [Python 3.x](https://www.python.org/downloads/) (for backend)
- [Pip](https://pip.pypa.io/en/stable/) (for Python package management)
- [TensorFlow](https://www.tensorflow.org/install) (for AI image analysis)
- [PyTorch](https://pytorch.org/get-started/locally/) (for AI image analysis)
- [YOLOv5](https://github.com/ultralytics/yolov5) (for object detection)

### Backend Setup (Python)

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/recipe-provider-web.git
    cd recipe-provider-web
    ```

2. Create a Python virtual environment:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the backend dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Install the necessary AI libraries:

    ```bash
    pip install tensorflow
    pip install torch torchvision
    pip install yolov5
    ```

5. Set up LangChain by following the official documentation to configure the AI model.

6. Set up a database (either MongoDB or PostgreSQL) to store user data, recipes, and AI-generated recommendations.

7. Run the backend server:

    ```bash
    python app.py  # Alternatively, use 'flask run' or 'uvicorn' based on your framework
    ```

### Frontend Setup (React)

1. Navigate to the `frontend` directory:

    ```bash
    cd frontend
    ```

2. Install Node.js dependencies:

    ```bash
    npm install
    ```

3. Start the React development server:

    ```bash
    npm start
    ```

4. Access the app at `http://localhost:3000`.

# Image Upload & Object Detection

- **YOLOv5 Object Detection:** Users upload images of ingredients or dishes, and the backend uses YOLOv5 for real-time object detection to identify the items in the image.
- **Ingredient Categorization:** Once ingredients are detected, TensorFlow and PyTorch analyze them to categorize them into food groups (e.g., "protein," "vegetable," "fruit") and estimate their nutritional content.

# API Endpoints

- **POST /api/recipes/image-recognition:** Receives an image, runs YOLOv5 object detection to identify ingredients, and returns a list of detected ingredients.
- **POST /api/recipes/recommendations:** Takes detected ingredients and user preferences to generate personalized recipe suggestions via LangChain.
- **GET /api/recipes/search:** Allows users to search for recipes by ingredient, cuisine, or dietary preferences.

# Running the Application

1. Start the backend server (if not already running).
2. Start the React frontend.
3. Open your browser and go to `http://localhost:3000`.

The application is now ready to provide personalized recipe recommendations, ingredient recognition, and intelligent recipe tagging based on your preferences and uploaded images.

# Contribution

Contributions are welcome! You can fork this repository and submit pull requests for bug fixes, new features, or improvements. When contributing, ensure that your code follows the project's coding standards and includes appropriate tests.

# License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Acknowledgements

- **LangChain:** For providing personalized recipe recommendations based on user preferences and ingredients.
- **YOLOv5:** For real-time object detection to identify ingredients and dishes from images.
- **TensorFlow and PyTorch:** For advanced image processing and classification tasks, such as ingredient categorization and nutritional analysis.
- **React:** For building the interactive and responsive frontend interface.
- **Flask/FastAPI:** For building the backend API that connects the frontend with AI models.
