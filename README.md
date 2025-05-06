# AI Body Measurement System

An advanced AI-powered system that accurately measures body dimensions and recommends clothing sizes using front and side view images.

## Features

- Accurate body measurement prediction using AI
- Background removal for clean image processing
- Support for both male and female measurements
- Clothing size recommendations (T-shirts and Pants)
- Web-based interface for easy interaction
- Real-time processing and results

## Supported Measurements

- Ankle
- Arm Length
- Bicep
- Calf
- Chest
- Forearm
- Height
- Hip
- Leg Length
- Shoulder Breadth
- Shoulder to Crotch
- Thigh
- Waist
- Wrist

## Prerequisites

- Python 3.8 or higher
- Web browser
- Camera or image capture device

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/AI-BodyMeasurement.git
cd AI-BodyMeasurement
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Start the server:
```bash
python main.py
```

2. Open your web browser and navigate to:
```
http://localhost:8000
```

3. Upload front and side view images of the person
4. Enter the required information:
   - Gender (0 for male, 1 for female)
   - Height (in cm)
   - Weight (in kg)
   - Apparel type (tshirt, pants, or all)

5. Submit and receive measurements and size recommendations

## API Endpoints

- `GET /`: Web interface
- `POST /predict/`: Prediction endpoint
  - Accepts multipart form data with:
    - front_image: Front view image
    - side_image: Side view image
    - input_data: JSON string containing gender, height, weight, and apparel type

## Project Structure

- `main.py`: FastAPI server and endpoint definitions
- `single_person_processor.py`: Core processing and prediction logic
- `best_model.keras`: Trained AI model
- `static/`: Static assets
- `templete.html`: Web interface template

