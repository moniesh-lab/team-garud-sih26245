# GTMS — AI Attendance & Training Center Monitoring System

An AI-powered Training Center Monitoring System designed to support classroom monitoring, student attendance verification, and equipment surveillance using computer vision.

GTMS integrates a web-based dashboard with YOLO-based person detection to monitor classroom occupancy, visualize detected people, and support more efficient training center administration.

## Features

### AI-Powered Classroom Monitoring
- YOLO-based person detection.
- Real-time or video-based classroom monitoring, depending on the configured camera source.
- Bounding-box visualization for detected people.
- Automatic headcount calculation.
- Detection performance testing using sample classroom videos.

### Attendance Monitoring
- AI-assisted classroom attendance monitoring.
- Headcount-based occupancy verification.
- Foundation for comparing AI-generated attendance with trainer-submitted manual attendance.

### Training Center Oversight
- Web-based monitoring dashboard.
- Sample video selection and detection visualization.
- Detection telemetry and model output inspection.
- Foundation for centralized government monitoring of training centers.

### Equipment Monitoring
- Computer vision experiments for equipment detection.
- Support for testing equipment-related detection scenarios.
- Potential extension for equipment inventory verification and damage reporting.

## Technology Stack

**Frontend**
- React
- Vite
- JavaScript / TypeScript, depending on the configured source files
- HTML and CSS

**AI and Backend**
- Python
- Ultralytics YOLO
- OpenCV and supporting computer vision libraries, where configured
- FFmpeg for video processing, where configured

## Project Structure

The project includes frontend source files, backend detection scripts, model weights, sample images, configuration files, and video-testing resources.

Typical components include:

- `src/` — frontend application source.
- `public/` — static frontend assets.
- `package.json` — frontend dependencies and scripts.
- `package-lock.json` — locked npm dependency versions.
- `vite.config.*` — Vite configuration.
- `yolo_camera_server.py` — Python camera and YOLO processing component.
- `yolov8n.pt` — pretrained YOLO model weights.
- Sample images and annotation/configuration files — resources for detection testing.

The exact contents may vary with the project version.

## Getting Started

### Prerequisites

Install the following software:

- Node.js and npm.
- Python compatible with the project's installed AI dependencies.
- Git, if cloning the repository.
- FFmpeg if required by the configured video-processing pipeline.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/GTMS-AI-Training-Monitoring.git
cd GTMS-AI-Training-Monitoring
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Install frontend dependencies

```bash
npm install
```

### 3. Start the frontend

```bash
npm run dev
```

Open the local URL displayed by Vite in your browser.

### 4. Configure the Python backend

Install the Python dependencies specified by the project's backend requirements file, if provided.

For example:

```bash
python -m venv .venv
```

On Windows:

```bash
.venv\Scripts\activate
```

Install the dependencies using the project's actual requirements file:

```bash
pip install -r requirements.txt
```

Start the backend using the entry point and command documented in the project. The exact command depends on how `yolo_camera_server.py` is implemented.

**Note:** Do not assume that the frontend and backend start together. Configure and run each service as required by the application.

## Model and Dataset

The project includes YOLO-related model and detection-testing resources.

Model performance depends on the selected weights, image resolution, training data, annotations, and inference configuration.

For reliable classroom person detection, use a representative, correctly labeled dataset containing:
- Students at different distances from the camera.
- Partially occluded people.
- Different classroom layouts and lighting conditions.
- Trainers and students in different postures.

Evaluate the model using held-out videos and manually verified reference counts before using its output for attendance decisions.

## Deployment

The frontend can be deployed to a compatible static web hosting platform such as Vercel if the build configuration is supported.

The Python YOLO backend generally requires a separate compatible hosting service or dedicated machine for persistent video processing.

When deploying:
1. Configure the frontend build command and output directory.
2. Deploy the Python backend separately where necessary.
3. Configure the frontend to use the deployed backend URL.
4. Configure camera access, model paths, environment variables, and CORS appropriately.
5. Test all application features after deployment.

Do not use `localhost` as the production API address.

## Privacy and Security

Classroom camera feeds and student information can contain sensitive personal data.

- Restrict access using appropriate authentication and authorization.
- Secure camera feeds and API endpoints.
- Avoid committing credentials, secret keys, or private student data.
- Use authorized datasets and camera recordings.
- Establish suitable data retention and access-control policies.

## Current Development Goals

- Improve person detection in dense classrooms.
- Reduce missed and duplicate detections.
- Improve headcount accuracy.
- Implement reliable video seeking and playback controls.
- Evaluate model performance on unseen classroom footage.
- Extend attendance verification and equipment monitoring.

## Disclaimer

GTMS is a computer vision and monitoring project under development. Detection results may be inaccurate due to occlusion, camera perspective, lighting, and model limitations.

AI detections should be independently verified before being used for consequential attendance or disciplinary decisions.

## License

Choose and add an appropriate open-source license before distributing the project. Ensure that the licenses of all included model weights, datasets, and third-party dependencies permit your intended use.

---

**GTMS — AI Attendance & Training Center Monitoring System**  
*Computer vision for smarter training center monitoring.*
