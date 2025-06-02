# Body Measurement System

A simple system that measures body dimensions and suggests clothing sizes using front and side view photos.

## Features

- Body measurements
- Clothing size recommendations
- Easy web interface
- 
[Screencast from 2025-04-26 18-02-00.webm](https://github.com/user-attachments/assets/7d9b662d-de3f-4cf1-9dbe-1aa26dde7baf)

## Setup

1. Install requirements:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

2. Run the server:
```bash
python main.py
```

3. Open http://localhost:8000 in your browser

## How to Use

1. Upload front and side view photos
2. Enter:
   - Gender (0 for male, 1 for female)
   - Height (cm)
   - Weight (kg)
   - Clothing type (shirt, pants, or all)
3. Click measure to get results

## License

MIT License

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
- Shoulder Width
- Shoulder to Hip
- Thigh
- Waist
- Wrist

## Support and Contributions

We welcome contributions! Feel free to open an issue or submit a pull request to help improve the project.

## Project Structure

- `main.py`: Server and API endpoints
- `single_person_processor.py`: Core measurement logic
- `best_model.keras`: Measurement model
- `static/`: Web interface files
- `template.html`: Web page template

## API Endpoints

- `GET /`: Web interface
- `POST /predict/`: Prediction endpoint
  - Accepts multipart form data with:
    - front_image: Front view image
    - side_image: Side view image
    - input_data: JSON string containing gender, height, weight, and apparel type

## Rights and License

This project is licensed under the MIT License - see the LICENSE file for details.
