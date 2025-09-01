# SuperGen - ML-Powered Startup Name Generator (Experimental)

![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)
![React](https://img.shields.io/badge/react-18+-61DAFB.svg)
![TypeScript](https://img.shields.io/badge/typescript-5+-3178C6.svg)
![Flask](https://img.shields.io/badge/flask-2.0+-000000.svg)
![Supabase](https://img.shields.io/badge/supabase-enabled-3ECF8E.svg)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-1.0+-F7931E.svg)
![Experimental](https://img.shields.io/badge/status-experimental-orange.svg)
![MIT License](https://img.shields.io/badge/license-MIT-green.svg)

An experimental machine learning-powered web application that generates memorable, brandable startup names using advanced natural language processing and predictive analytics.

## Application Flow

### Landing Page
<img width="3414" height="2128" alt="image" src="https://github.com/user-attachments/assets/88045834-aef0-46f6-9f1f-252eed8adb30" />

### Signin Page
<img width="3402" height="2116" alt="image" src="https://github.com/user-attachments/assets/526c687b-7396-4627-9e6a-859826b91a42" />

### Dashboard
<img width="3402" height="2120" alt="image" src="https://github.com/user-attachments/assets/b9276278-9e30-41d8-a2e4-acf0ae20dbfa" />

### Generate Names 
<img width="3402" height="2124" alt="image" src="https://github.com/user-attachments/assets/2faf328a-5c85-4ef8-a573-4882671f13a9" />

### Analyze Names 
<img width="3408" height="2120" alt="image" src="https://github.com/user-attachments/assets/9ec7e6e6-22c6-4986-9fb3-40d23de1c6bb" />

### Model Analysis Names 
<img width="3416" height="2124" alt="image" src="https://github.com/user-attachments/assets/5f6d39bf-96ba-431f-9a85-20da6d6fce10" />

## Features

### Core Functionality
- **ML-Powered Generation**: RandomForest models predict name success probability based on successful startup datasets
- **Industry-Specific Suggestions**: Tailored naming patterns for Tech, Fintech, Healthcare, SaaS, AI, and E-commerce
- **Comprehensive Name Analysis**: Scoring for pronounceability, memorability, and market fit
- **Similar Name Discovery**: Find names similar to successful brands using TF-IDF vectorization and K-means clustering

### Name Generation Strategies
- Compound word combinations (AirBnb, PayPal style)
- Tech-style suffixes (-ly, -ify, -io, -hub)
- Invented brandable words (Google, Spotify style)
- Portmanteau blending techniques
- Rhythmic sound pattern optimization

### Analytics & Insights
- **Feature Engineering**: 25+ linguistic and semantic features per name
- **Success Prediction**: ML models trained on unicorn company naming patterns
- **Availability Check**: Domain, trademark, and social media availability estimation
- **Feature Importance**: Analysis of which characteristics drive naming success

## Technology Stack

### Backend
- **Flask**: RESTful API with CORS support
- **Supabase**: PostgreSQL database with real-time authentication and RLS
- **Scikit-learn**: RandomForest classification and regression models
- **NLTK**: Natural language processing and sentiment analysis
- **Pandas/NumPy**: Data manipulation and feature engineering
- **TextStat**: Readability and linguistic complexity analysis

### Frontend
- **React/TypeScript**: Component-based UI with type safety
- **Supabase Client**: Real-time authentication and database integration
- **Tailwind CSS**: Responsive design with modern styling
- **Lucide React**: Consistent icon library

### ML Pipeline (Experimental)
- **Feature Extraction**: Experimental syllable counting, character patterns, sentiment analysis
- **Model Training**: Prototype RandomForest classifier for success prediction, regressor for scoring
- **Text Vectorization**: Experimental TF-IDF character-level and word-level analysis
- **Clustering**: K-means clustering for naming pattern similarities (beta)

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/health` | GET | Health check with model status |
| `/api/generate-names` | POST | Generate startup names with ML scoring |
| `/api/analyze-name` | POST | Comprehensive name analysis |
| `/api/similar-names` | POST | Find similar names using clustering |
| `/api/feature-importance` | GET | ML model feature importance insights |

### Database Schema
```sql
-- Supabase profiles table
CREATE TABLE profiles (
  id UUID REFERENCES auth.users(id) PRIMARY KEY,
  email TEXT NOT NULL,
  full_name TEXT,
  company TEXT,
  avatar_url TEXT,
  subscription_tier TEXT DEFAULT 'free',
  credits_remaining INTEGER DEFAULT 3,
  created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW(),
  updated_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Row Level Security enabled
ALTER TABLE profiles ENABLE ROW LEVEL SECURITY;
```

### Prerequisites
- Python 3.8+
- Node.js 16+
- npm or yarn

### Backend Setup
```bash
# Install Python dependencies
pip install flask flask-cors scikit-learn nltk pandas numpy textstat python-dotenv

# Start the Flask server
python app/main.py
```

### Frontend Setup
```bash
# Install dependencies
npm install

# Set environment variables
echo "REACT_APP_API_BASE=http://localhost:5000" > .env
echo "REACT_APP_SUPABASE_URL=your_supabase_url" >> .env
echo "REACT_APP_SUPABASE_ANON_KEY=your_supabase_anon_key" >> .env

# Start development server
npm start
```

### Environment Configuration
```bash
# .env file
REACT_APP_API_BASE=http://localhost:5000
REACT_APP_SUPABASE_URL=https://your-project-id.supabase.co
REACT_APP_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## Model Training (Experimental)

The system experimentally trains ML models on startup using:
- 30+ successful startup examples (Google, Apple, Stripe, etc.)
- Generated negative examples for balanced training
- 25+ linguistic feature extraction techniques
- Prototype RandomForest models for classification and regression

**Note**: This is experimental research software. The ML models are prototypes and naming success predictions should be considered as experimental insights rather than definitive business advice.

## Performance Metrics

- **Generation Speed**: 10-20 names in under 2 seconds
- **Model Accuracy**: ~80% on validation data
- **Real-time Analysis**: Instant name scoring and feedback
- **Scalable Architecture**: Supports high-traffic deployment

## Application Screenshots

The application includes:
- Clean landing page with feature overview
- Secure authentication system
- Interactive dashboard with multiple analysis tools
- Real-time name generation and scoring
- Comprehensive name analysis with ML insights

## Use Cases

- Startup founders seeking data-driven naming decisions
- Marketing agencies developing brand identities
- Entrepreneurs validating existing name choices
- Researchers studying startup naming patterns

## Development

### Local Development
1. Start Flask backend on port 5000
2. Start React frontend on port 3000
3. Ensure CORS is configured for localhost:3000
4. Verify API connectivity via health endpoint

### Deployment
- Backend: Compatible with any WSGI server
- Frontend: Static build deployable to any CDN
- Database: Optional Supabase integration for user profiles
