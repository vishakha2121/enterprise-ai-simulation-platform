# 🏢 Enterprise AI Simulation Platform

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.68+-green.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18.0+-blue.svg)](https://reactjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13+-orange.svg)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## 📋 Table of Contents
- [Overview](#-overview)
- [Core Problem Solved](#-core-problem-solved)
- [Key Technologies](#-key-technologies)
- [Features](#-features)
- [Technology Stack](#-technology-stack)
- [Architecture](#-architecture)
- [Database Schema](#-database-schema)
- [Installation Guide](#-installation-guide)
- [Configuration](#-configuration)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Testing](#-testing)
- [Deployment](#-deployment)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

**Enterprise AI Simulation Platform** is an intelligent decision-support system that leverages cutting-edge AI technologies to help businesses evaluate strategic decisions before implementation. By combining **Digital Twin technology**, **Monte Carlo simulations**, and **Reinforcement Learning**, the platform creates a safe virtual environment where organizations can test business strategies, predict outcomes, and optimize operations without risking real-world resources.

### 🎥 Demo
> **Coming Soon**: Live demo link will be available here

---

## 💡 Core Problem Solved

Every day, business leaders make critical decisions about:
- 📈 Investments and capital allocation
- 🏭 Operations and supply chain management
- 👥 Resource allocation and workforce planning
- 📊 Strategic planning and market expansion
- 💰 Pricing strategies and revenue optimization

**Traditional decision-making** relies on:
- ❌ Intuition and gut feeling
- ❌ Historical data without future context
- ❌ Simple predictive models that miss complexity
- ❌ Static analysis without dynamic interactions

**Our Solution**:
- ✅ Virtual replicas of business operations
- ✅ Thousands of scenario simulations
- ✅ AI-driven optimal strategy learning
- ✅ Data-driven insights for confident decisions
- ✅ Risk quantification and uncertainty analysis

---

## 🚀 Key Technologies

### 1. Digital Twin Technology 🖥️
**Purpose**: Creates a virtual mirror of your business operations

| Feature | Description |
|---------|-------------|
| **Real-time Sync** | Synchronizes with business processes |
| **Entity Mapping** | Maps customers, suppliers, employees, resources |
| **State Monitoring** | Tracks dynamic states and changes |
| **Scenario Testing** | Tests what-if scenarios safely |
| **Predictive Analysis** | Predicts future states and outcomes |

### 2. Monte Carlo Simulations 🎲
**Purpose**: Quantifies uncertainty and risk in business decisions

| Feature | Description |
|---------|-------------|
| **Probabilistic Modeling** | Models uncertainty in outcomes |
| **Risk Assessment** | Quantifies risk and confidence |
| **Scenario Generation** | Thousands of variations |
| **Sensitivity Analysis** | Identifies key drivers |
| **ROI Prediction** | Predicts returns with uncertainty |

### 3. Reinforcement Learning 🤖
**Purpose**: Learns optimal strategies through trial and error

| Feature | Description |
|---------|-------------|
| **Self-improvement** | Learns from simulation outcomes |
| **Policy Optimization** | DQN, PPO, A2C algorithms |
| **Reward Design** | Custom business objectives |
| **Continuous Learning** | Adapts to new data |
| **Strategy Recommendations** | Optimal action suggestions |

### 4. Gemini API Integration 🧠
**Purpose**: Provides natural language intelligence

| Feature | Description |
|---------|-------------|
| **NLP Queries** | Natural language business queries |
| **Insight Generation** | Automated insights from data |
| **Decision Support** | Smart recommendations |
| **Report Writing** | Automated business reports |
| **Scenario Analysis** | Natural language scenario analysis |

---

## ✨ Features

### 🔐 Authentication & Security
- JWT-based authentication
- Role-based access control
- Password hashing with bcrypt
- Session management
- Audit logging

### 📊 Dashboard & Analytics
- Real-time business metrics
- Interactive charts and graphs
- Customizable dashboards
- Export reports (PDF, CSV, JSON)
- Performance KPIs tracking

### 🏗️ Digital Twin Module
- Business entity management
- Relationship mapping
- State synchronization
- What-if scenario testing
- Virtual simulation environment

### 🎲 Monte Carlo Module
- Custom distribution models
- Multi-variable analysis
- Confidence interval calculation
- Risk assessment reports
- Scenario comparison

### 🤖 Reinforcement Learning Module
- Multiple RL algorithms
- Custom reward functions
- Training progress visualization
- Policy comparison
- Decision recommendation

### 🧠 Gemini AI Integration
- Natural language interface
- Smart business insights
- Automated reporting
- Trend analysis
- Recommendation engine

### 📱 User Interface
- Responsive design
- Dark/Light theme
- Real-time updates
- Interactive visualizations
- Drag-and-drop functionality

---

## 🛠️ Technology Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18.0+ | UI Framework |
| **Tailwind CSS** | 3.0+ | Styling |
| **D3.js** | 7.0+ | Data Visualization |
| **Chart.js** | 4.0+ | Charts |
| **WebSocket** | - | Real-time updates |
| **Axios** | 1.0+ | HTTP Client |
| **React Router** | 6.0+ | Routing |
| **Redux Toolkit** | 1.9+ | State Management |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| **FastAPI** | 0.68+ | Web Framework |
| **Python** | 3.9+ | Programming Language |
| **PostgreSQL** | 13+ | Database |
| **SQLAlchemy** | 1.4+ | ORM |
| **Alembic** | 1.7+ | Migrations |
| **Redis** | 6.0+ | Caching |
| **Celery** | 5.0+ | Background Tasks |
| **JWT** | - | Authentication |

### AI/ML Libraries
| Technology | Version | Purpose |
|------------|---------|---------|
| **NumPy** | 1.21+ | Numerical Computing |
| **Pandas** | 1.3+ | Data Analysis |
| **Scikit-learn** | 1.0+ | ML Algorithms |
| **TensorFlow** | 2.8+ | Deep Learning |
| **PyTorch** | 1.10+ | Deep Learning |
| **Gymnasium** | 0.26+ | RL Environments |
| **Stable-Baselines3** | 1.6+ | RL Algorithms |

### External APIs
| API | Purpose |
|-----|---------|
| **Google Gemini** | NLP and Insights |

---

## 🏗️ Architecture

---

## 📊 Database Schema

### Core Tables
```sql
-- Users and Authentication
users (
    id UUID PRIMARY KEY,
    username VARCHAR(50) UNIQUE,
    email VARCHAR(100) UNIQUE,
    password_hash VARCHAR(255),
    role VARCHAR(20),
    created_at TIMESTAMP,
    updated_at TIMESTAMP
)

-- Simulation Management
simulations (
    id UUID PRIMARY KEY,
    name VARCHAR(100),
    description TEXT,
    type VARCHAR(20),
    parameters JSON,
    status VARCHAR(20),
    user_id UUID REFERENCES users(id),
    created_at TIMESTAMP,
    completed_at TIMESTAMP
)

simulation_results (
    id UUID PRIMARY KEY,
    simulation_id UUID REFERENCES simulations(id),
    results JSON,
    metrics JSON,
    confidence_interval JSON,
    created_at TIMESTAMP
)

-- Digital Twin
digital_twins (
    id UUID PRIMARY KEY,
    name VARCHAR(100),
    description TEXT,
    user_id UUID REFERENCES users(id),
    status VARCHAR(20),
    sync_status VARCHAR(20),
    created_at TIMESTAMP,
    updated_at TIMESTAMP
)

digital_twin_entities (
    id UUID PRIMARY KEY,
    digital_twin_id UUID REFERENCES digital_twins(id),
    entity_type VARCHAR(50),
    entity_data JSON,
    relationships JSON,
    created_at TIMESTAMP,
    updated_at TIMESTAMP
)

-- Monte Carlo
monte_carlo_simulations (
    id UUID PRIMARY KEY,
    name VARCHAR(100),
    description TEXT,
    simulation_id UUID REFERENCES simulations(id),
    num_scenarios INTEGER,
    parameters JSON,
    distributions JSON,
    created_at TIMESTAMP
)

monte_carlo_results (
    id UUID PRIMARY KEY,
    monte_carlo_id UUID REFERENCES monte_carlo_simulations(id),
    results JSON,
    statistics JSON,
    percentiles JSON,
    created_at TIMESTAMP
)

-- Reinforcement Learning
rl_agents (
    id UUID PRIMARY KEY,
    name VARCHAR(100),
    algorithm VARCHAR(50),
    parameters JSON,
    state_dim INTEGER,
    action_dim INTEGER,
    created_at TIMESTAMP
)

rl_training_sessions (
    id UUID PRIMARY KEY,
    agent_id UUID REFERENCES rl_agents(id),
    simulation_id UUID REFERENCES simulations(id),
    episodes INTEGER,
    total_reward FLOAT,
    training_time INTEGER,
    created_at TIMESTAMP
)

rl_episodes (
    id UUID PRIMARY KEY,
    session_id UUID REFERENCES rl_training_sessions(id),
    episode_number INTEGER,
    rewards JSON,
    actions JSON,
    states JSON,
    total_reward FLOAT,
    created_at TIMESTAMP
)

-- Business Metrics
business_metrics (
    id UUID PRIMARY KEY,
    name VARCHAR(50),
    value FLOAT,
    timestamp TIMESTAMP,
    simulation_id UUID REFERENCES simulations(id)
)

-- Audit Logs
audit_logs (
    id UUID PRIMARY KEY,
    user_id UUID REFERENCES users(id),
    action VARCHAR(50),
    details JSON,
    timestamp TIMESTAMP
)# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Install development dependencies (optional)
pip install -r requirements-dev.txt

# Create .env file
cp .env.example .env

# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env