# SuperGen - AI-Powered Startup Name Generator

SuperGen is a machine learning-powered web application that generates memorable, brandable startup names using advanced natural language processing and predictive analytics. Built for entrepreneurs who need data-driven naming solutions.


## Application Flow

### Landing Page
<img width="1467" height="786" alt="landing-page" src="https://github.com/user-attachments/assets/63ee147d-b0ab-4d4e-bbbe-6da6c73bba80" />

### Signup Page
<img width="1462" height="798" alt="Screenshot 2025-09-01 at 1 03 18 pm" src="https://github.com/user-attachments/assets/3f8eb791-6e94-41a0-8880-f79976dfc721" />

### Dashboard
<img width="1467" height="786" alt="dashboard" src="https://github.com/user-attachments/assets/63ee147d-b0ab-4d4e-bbbe-6da6c73bba80" />

## Features

### Core Functionality
- **ML-Powered Generation**: RandomForest models trained on successful startup datasets predict name success probability
- **Industry-Specific Suggestions**: Tailored naming patterns for Tech, Fintech, Healthcare, SaaS, AI, and E-commerce
- **Advanced Name Analysis**: Comprehensive scoring including pronounceability, memorability, and market fit
- **Clustering-Based Similar Names**: Find names similar to successful brands using TF-IDF vectorization and K-means clustering

### Name Generation Strategies
- Compound word combinations (like AirBnb, PayPal)
- Tech-style suffixes (-ly, -ify, -io, -hub)
- Invented brandable words (like Google, Spotify)
- Portmanteau blending techniques
- Rhythmic sound pattern optimization

### Analytics & Insights
- **Feature Engineering**: 25+ linguistic and semantic features per name
- **Success Prediction**: ML models trained on unicorn company naming patterns
- **Availability Simulation**: Domain, trademark, and social media availability estimation
- **Feature Importance Analysis**: Understand which characteristics drive naming success

## Technology Stack

### Backend
- **Flask**: RESTful API with CORS support
- **Scikit-learn**: RandomForest classification and regression models
- **NLTK**: Natural language processing and sentiment analysis
- **Pandas/NumPy**: Data manipulation and feature engineering
- **TextStat**: Readability and linguistic complexity analysis

### Frontend
- **React/TypeScript**: Modern component-based UI
- **Tailwind CSS**: Responsive design with glassmorphism effects
- **Lucide React**: Icon library for consistent UI elements

### ML Pipeline
- **Feature Extraction**: Syllable counting, character patterns, sentiment analysis
- **Model Training**: RandomForest classifier for success prediction, regressor for scoring
- **Text Vectorization**: TF-IDF character-level and word-level analysis
- **Clustering**: K-means for finding naming pattern similarities

## API Endpoints

- `POST /api/generate-names` - Generate startup names with ML scoring
- `POST /api/analyze-name` - Comprehensive name analysis
- `POST /api/similar-names` - Find names similar to reference using clustering
- `GET /api/feature-importance` - ML model feature importance insights
- `GET /api/health` - Health check with model status

## Model Training

The system automatically trains ML models on startup using:
- 30+ successful startup examples (Google, Apple, Stripe, etc.)
- Generated negative examples for balanced training
- Feature engineering with 25+ linguistic characteristics
- RandomForest models for classification and regression tasks

## Use Cases

- Startup founders seeking data-driven naming decisions
- Marketing agencies developing brand identities
- Entrepreneurs validating existing name choices
- Researchers studying startup naming patterns

## Performance

- Generates 10-20 names in under 2 seconds
- ML model accuracy: ~80% on test data
- Supports real-time name analysis and scoring
- Scalable architecture for high-traffic deployment
