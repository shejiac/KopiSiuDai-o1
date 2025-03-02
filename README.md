# KopiSiuDai-o1
Dear judges, please download this codebase and dataset of https://drive.google.com/file/d/1Hjd82dJZKcUsNMR-7_o6mHXZ72ibfl3P/view?usp=sharing .
Thank you so much.

# Sortee - AI-Powered Waste Classification

Sortee is an AI-powered waste classification tool that uses TensorFlow.js to help users correctly identify and sort waste items. The application provides real-time classification through webcam input and supports model fine-tuning directly in the browser.

## Features

- **Real-time Webcam Classification**: Classify waste items in real-time using your webcam
- **Browser-based Model Fine-tuning**: Improve model accuracy directly in your browser
- **Responsive UI**: Modern, user-friendly interface that works on desktop and mobile devices

## Getting Started

### Prerequisites

- Node.js (v14 or later)
- npm or yarn
- TrashNet dataset (included in the repository)

### Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/sortee.git
   cd sortee
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Run the development server:
   ```
   npm run dev
   ```

4. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

## Model Training and Fine-tuning

### Training the Base Model

The base model is trained using the TrashNet dataset. To train the model from scratch:

```
npm run model-pipeline
```

This command runs the following steps:
1. Sets up the environment
2. Prepares the dataset
3. Trains the model
4. Converts the model for browser use

### Fine-tuning the Model

There are two ways to fine-tune the model:

#### 1. Browser-based Fine-tuning (Recommended)

The easiest way to fine-tune the model is directly in your browser:

1. Start the development server:
   ```
   npm run dev
   ```

2. Navigate to the fine-tuning page:
   ```
   http://localhost:3000/fine-tune
   ```

3. Follow the on-screen instructions to:
   - Load the pre-trained model
   - Start the fine-tuning process
   - Save the fine-tuned model to browser storage

This approach uses synthetic data for demonstration purposes. In a real-world scenario, you would use your own labeled images.

#### 2. Server-side Fine-tuning (Advanced)

For more advanced fine-tuning with your own dataset:

```
npm run run-fine-tuning
```

Note: This requires additional setup and may have compatibility issues with newer Node.js versions.

## Using the Webcam Classifier

1. Start the development server:
   ```
   npm run dev
   ```

2. Navigate to the webcam classifier page:
   ```
   http://localhost:3000/webcam-classifier
   ```

3. Allow camera access when prompted
4. Point your camera at waste items to classify them
5. View the classification results in real-time

## Project Structure

```
sortee/
├── components/         # React components
├── data/               # Dataset and model files
│   └── trashnet/       # TrashNet dataset
├── pages/              # Next.js pages
│   ├── index.js        # Home page
│   ├── webcam-classifier.js  # Webcam classifier page
│   └── fine-tune.js    # Fine-tuning page
├── public/             # Static files
│   └── model/          # Trained model files
├── scripts/            # Training and fine-tuning scripts
├── styles/             # CSS styles
├── package.json        # Project dependencies
└── README.md           # This file
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- [TrashNet dataset](https://github.com/garythung/trashnet) for providing the waste classification dataset
- [TensorFlow.js](https://www.tensorflow.org/js) for enabling machine learning in the browser
- [Next.js](https://nextjs.org/) for the React framework 
