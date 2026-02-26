# EcoScanApp 🌱

A sustainability assistant that scans product barcodes to analyze carbon footprint and recommends eco-friendly alternatives when emissions are above threshold.

## Features

- **Barcode Scanning**: Upload, drag-and-drop, or use camera to scan product barcodes
- **Carbon Footprint Analysis**: Real-time data from Open Food Facts API
- **Smart Recommendations**: Personalized sustainability insights
- **Alternative Products**: Suggests eco-friendlier options when carbon footprint is high
- **Beautiful UI**: Modern, responsive design with smooth animations

## Tech Stack

### Frontend
- **Vite** - Fast build tool
- **React 18** - UI library
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **Lucide React** - Icons

### Backend
- **FastAPI** - Modern Python API framework
- **Pydantic** - Data validation
- **httpx** - Async HTTP client
- **pyzbar + Pillow** - Barcode detection

## Getting Started

### Backend Setup

```bash
cd backend
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Mac/Linux
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/scan` | Scan barcode image and get product data |
| GET | `/api/product/{gtin}` | Get product by barcode number |
| GET | `/health` | Health check |

## Environment Variables

**Backend** - Create `.env` in backend folder:
```
USER_AGENT=EcoScanApp/1.0 (your-email@example.com)
```

**Frontend** - Create `.env` in frontend folder (optional):
```
VITE_API_URL=http://localhost:8000
```

## Test Barcodes

Use these GTINs for testing:

- Coca-Cola: `5449000000996`
