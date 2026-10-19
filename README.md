# DRISHTI — AI-Powered Government Training Monitoring System

### DRISHTI | Team GARUD | SIH26245

**Live Demo:** https://drishti-garud8.vercel.app  
**GitHub Repository:** https://github.com/moniesh-lab/DRISHTI-SIH26245_GARUD

---

## About the Project

**DRISHTI** is an AI-powered monitoring and compliance platform designed to support transparent, efficient, and data-driven oversight of government training centres.

The system brings together computer vision-based trainee monitoring, attendance verification, infrastructure and equipment auditing, and compliance tracking in a centralized dashboard. It aims to help authorities identify discrepancies, monitor training-centre performance, and make informed inspection decisions.

## Key Features

- **AI-Powered Attendance Monitoring:** Uses YOLO-based computer vision to support trainee detection and attendance verification.
- **CCTV Video Monitoring:** Displays camera feeds and sample CCTV footage for training-centre monitoring.
- **Multi-Centre Dashboard:** Provides a centralized interface for monitoring multiple training centres.
- **Attendance Discrepancy Detection:** Compares reported attendance with AI-detected counts.
- **Equipment and Infrastructure Auditing:** Tracks sanctioned equipment, detected quantities, shortages, and reported defective assets.
- **Compliance Monitoring:** Highlights potential compliance issues and supports configurable monitoring thresholds.
- **Inspection Support:** Provides inspection alerts, audit information, and review actions.
- **Audit Data Export:** Allows dashboard audit information to be exported in JSON format.
- **Interactive Dashboard:** Presents monitoring information through a structured, responsive interface.

## Technology Stack

| Technology | Purpose |
|---|---|
| React | User interface |
| Vite | Frontend development and build tooling |
| JavaScript / JSX | Application logic and components |
| Tailwind CSS | Dashboard styling |
| Lucide React | Interface icons |
| YOLO-based computer vision | Trainee and object detection |
| Vercel | Frontend deployment |

*The technology list describes the known frontend and monitoring components; additional backend or model-serving technologies may be used depending on the project configuration.*

## System Overview

The platform follows a monitoring and verification workflow:

1. Select a training centre from the dashboard.
2. View its available camera feed or sample CCTV footage.
3. Review AI-detected trainee counts and compare them with reported attendance.
4. Inspect equipment availability, shortages, and reported defects.
5. Review compliance indicators and potential inspection requirements.
6. Export audit information for further review.

## Getting Started

### Prerequisites

- Node.js and npm
- Git
- A modern web browser

### 1. Clone the repository

```bash
git clone https://github.com/moniesh-lab/DRISHTI-SIH26245_GARUD.git
```

### 2. Navigate to the frontend directory

```bash
cd DRISHTI-SIH26245_GARUD/gov-monitoring-system
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
npm run dev
```

Open the local URL displayed in your terminal to access the dashboard.

### 5. Create a production build

```bash
npm run build
```

The generated production files will be available in the `dist` directory.

## Deployment

The deployed dashboard is available here:

**[Open DRISHTI Live Demo](https://drishti-garud8.vercel.app)**

The frontend is deployed using Vercel. Ensure that the required static assets are included in the deployment and that any external services or backend endpoints required by the application are correctly configured.

## Project Structure

```text
DRISHTI-SIH26245_GARUD/
├── gov-monitoring-system/
│   ├── public/                 # Static assets and sample media
│   ├── src/
│   │   ├── components/         # Dashboard and monitoring components
│   │   ├── services/           # Application services
│   │   └── ...                 # Application source files
│   ├── package.json
│   └── vite.config.js
├── .gitignore
├── .vercelignore
└── README.md
```

*This is a simplified overview; the exact directory structure may vary across versions.*

## Intended Impact

DRISHTI aims to improve government training-centre oversight by bringing attendance verification, infrastructure monitoring, and compliance information into one interface.

Its intended benefits include:

- Better visibility into training-centre operations.
- Faster identification of attendance discrepancies.
- Improved tracking of equipment shortages and defects.
- More structured compliance reviews and inspection workflows.
- Greater transparency and accountability through centralized monitoring.

## Limitations

- Detection accuracy depends on video quality, camera placement, lighting, and model performance.
- Sample CCTV footage demonstrates the monitoring interface but does not constitute a live camera connection.
- AI-generated counts should be reviewed before being used for official decisions.
- Compliance alerts support review and should not automatically be treated as proof of a violation.

## Future Enhancements

- Real-time CCTV stream integration.
- Improved detection accuracy under challenging lighting and occlusion.
- Historical analytics and trend visualization.
- Role-based access control and secure audit logging.
- Integration with verified government datasets and reporting systems.
- Automated generation of centre-wise compliance reports.

## Team

**Team GARUD**  
Project: DRISHTI  
Smart India Hackathon — SIH26245

## License

No license has been specified yet. Unless a license is added to the repository, reuse and redistribution are subject to the applicable copyright rules.

---

**DRISHTI — Vision for a Trusted Tomorrow.**
