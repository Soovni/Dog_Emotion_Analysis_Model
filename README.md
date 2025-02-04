(ENG) 
## Guess My Mood!

![Image](https://github.com/user-attachments/assets/484aa3ba-e0d4-4e88-a1ec-4858f36d8929){: width="30%" height="30%"}


### Happy, Sad, Sleepy, Playful, Scared…
### Building a Model to Predict Our Furry Friend’s Mood!
#### 1. What is CNN?
So far, we have worked on numerical and categorical data, setting independent and dependent variables to make predictions using models (e.g., Titanic dataset, first-phase inference).

But what about images? We live in an era filled with YouTube, Netflix, Instagram Reels, TV, and photos—can AI learn from image data?

#### Applications of Image & Video Analysis
Medical Imaging: Detecting brain tumors in MRI scans.
Autonomous Vehicles: Recognizing pedestrians, vehicles, and roads.
Traffic Analysis: Real-time congestion detection on highways.
Security & Surveillance: Detecting human presence in restricted areas via CCTV (e.g., construction sites, banks, homes).
Weather Forecasting: Analyzing cloud and storm patterns to predict damage and weather conditions.
Dietary Analysis: Estimating calorie intake from food images.
Applications of Image Generation
Style Transfer: Training AI to paint in the style of Van Gogh.
Fashion Design: Generating new clothing designs.
Personal Styling: Simulating how new hairstyles would look on an individual.
#### 2. How Does AI Learn from Images?

![Image](https://github.com/user-attachments/assets/1dc34df6-cd3e-4423-b8cf-0ecb279b2f25){: width="30%" height="30%"}

If we directly input this image into a fully connected layer, the AI will only perceive it as a 2D numerical matrix rather than an actual dog.



This means the AI cannot learn the characteristics of a dog effectively.

Humans recognize a dog in a picture by identifying its features. However, if we train AI using just a fully connected layer, it will also learn unnecessary background details (grass, people, etc.), making feature extraction ineffective.

#### 3. Convolutional Neural Networks (CNNs) and Feature Extraction
CNN is a technique that helps AI learn feature information from images.

![Illustration of CNN feature extraction with a moving filter.]

CNN scans an image using a small filter and learns distinct features such as:

The nose is positioned between the eyes.
Ears are located beside the eyes.
The nose and mouth are close to each other.
This scanning method, called convolution, extracts meaningful patterns while ignoring irrelevant background details.

#### 4. Collecting Images for Each Category
![Various dog images categorized by emotions such as happy, sad, and sleepy.]

#### 5. Training a CNN-Based Model for Dog Emotion Classification
In a CNN model, we can customize:

The number of convolutional layers
Pooling and stride settings
This flexibility allows us to create different image classification models.

Popular CNN Architectures
VGGNet
![Illustration of VGGNet structure.]

ResNet
![Illustration of ResNet structure.]

We can experiment with VGGNet, GoogleNet, and ResNet and adjust CNN parameters to build an optimal classification model.

#### 6. Training the Model & Testing on Real Data
After training, we can test the model on real-life pet dogs from the Insight research group to predict their emotions!

#### Key Steps in the Project
1. Defining Labels for Dog Emotions
Emotion categories: Happy, Sad, Sleepy, Scared, etc.
Selecting appropriate labels for classification.
2. Collecting Image Data
Using Unsplash API to download images.
Some categories may have fewer images (e.g., "scared" or "sleepy" might be harder to find).
Handling ambiguous images (e.g., Is the dog angry or just sleepy?):
Option 1: Remove uncertain images and use only clear data.
Option 2: Use an image generation model to create more clear samples.
Using Kaggle Dog Emotion Dataset:
Dog Emotion Dataset.
3. Standardizing Image Size
All images must be resized to the same dimensions before training CNN models.
4. Training CNN Models
Using pre-trained models (VGGNet, ResNet) for transfer learning to train and test the model.
Implementing custom CNNs with manual pooling and convolutional layers.
5. Deploying the Model
Once a well-performing model is developed, we deploy it using Streamlit or an application interface.
This project aims to build and test a CNN-based emotion classification model for dogs using real-world image data! 🚀🐶


