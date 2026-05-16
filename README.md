# Football BDA Backend

## Overview

Football BDA Backend is a football analytics backend system developed using Flask, PySpark, Docker, and REST APIs. The project provides football analytics, live scores, fixtures, standings, team/player statistics, match events, and match prediction features through a scalable backend architecture.

The system combines PySpark-based data processing with live football API integration and custom analytics services to deliver real-time football insights and predictions.

This project was developed as part of a collaborative team project consisting of 5 members. My main contributions focused on backend development, analytics integration, and especially the implementation of the match prediction functionality.

---

## Features

* Team rankings and analytics
* Team comparison system
* Player comparison system
* Live football scores
* Fixtures and schedules
* League standings
* Team statistics
* Player statistics
* Match event tracking
* Match prediction system
* REST API architecture
* PySpark data processing
* Docker containerization
* Mock data fallback system

---

## Technologies Used

* Python
* Flask
* PySpark
* Docker
* REST APIs
* Pandas
* NumPy
* JSON
* API-Football

---

## Project Structure

```bash id="r4x8pl"
football_bda/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── backend/
│   ├── api/
│   │   ├── app.py
│   │   └── client.py
│   │
│   ├── spark_jobs/
│   │   └── data_processor.py
│   │
│   └── services/
│       ├── analytics_service.py
│       └── mock_data.py
│
├── data/
│
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
├── .env
│
└── screenshots/
```

---

## Main Functionalities

### Team Rankings

Rank teams based on:

* Match performance
* Pass accuracy
* Shots
* Team statistics

### Team Comparison

Compare two teams side-by-side using:

* Match stats
* Possession
* Passing accuracy
* Offensive performance

### Player Comparison

Compare players using:

* Goals
* Assists
* Match statistics
* Performance metrics

### Live Football Data

* Live scores
* Fixtures
* Standings
* Team stats
* Player stats
* Match events

### Match Prediction

The backend includes a hybrid match prediction system that combines:

* Processed PySpark analytics data
* Team statistics
* League standings
* Live football context

I contributed significantly to the match prediction functionality and backend analytics integration.

---

## API Endpoints

### Health Check

```http id="v7m2qt"
GET /api/health
```

### Team Rankings

```http id="m3x8pl"
GET /api/rankings?limit=20
```

### Team Comparison

```http id="u6k1wr"
POST /api/teams/compare
```

### Player Comparison

```http id="t9q4xn"
POST /api/players/compare
```

### Live Scores

```http id="p5v7ks"
GET /api/live/scores
```

### Fixtures

```http id="z2m8ql"
GET /api/live/fixtures
```

### Match Prediction

```http id="n4x1wp"
GET /api/predict/match?fixture=215662
```

---

## How to Run the Project

### Option 1 — Local Development

1. Install Python

2. Install dependencies:

```bash id="j8v2tr"
pip install -r requirements.txt
```

3. Run the backend:

```bash id="k1x7pm"
python backend/api/app.py
```

4. Open:

```bash id="f9m3wl"
http://localhost:5000
```

---

### Option 2 — Docker

Run:

```bash id="r6q2vk"
docker-compose up --build
```

---

## Data Setup

Place the football dataset inside:

```bash id="u3w8xt"
data/
```

Expected dataset includes:

* Match data
* Team data
* Player statistics
* Match events

If no dataset is available, the system automatically uses mock data for testing.

---

## Docker Services

### Spark Master

* Port: 7077
* Web UI: http://localhost:8080

### Spark Worker

* Web UI: http://localhost:8081

### API Service

* Endpoint: http://localhost:5000

---

## Challenges

* Processing large football datasets
* Integrating real-time APIs
* Match prediction accuracy
* PySpark optimization
* Backend scalability
* Docker orchestration

---

## Future Improvements

* Full frontend integration
* Advanced AI match prediction
* Cloud deployment
* Real-time notifications
* User authentication
* HDFS integration
* Additional Spark workers

---

## Team Contribution

This project was developed by a team of 5 members.

My contributions included:

* Backend development
* REST API implementation
* Football analytics integration
* PySpark data processing support
* Match prediction system implementation
* Backend architecture improvements
* API integration and testing

I contributed significantly to the backend logic and played a major role in developing the match prediction functionality and analytics workflow.

---

## Author

Tarek Rajab

---

## License

This project is licensed under the MIT License.
