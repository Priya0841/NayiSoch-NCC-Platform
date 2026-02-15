# NCC Cadet Growth Intelligence Platform

> An AI-powered digital ecosystem for India's National Cadet Corps to centralize cadet data and provide intelligent growth recommendations.

## 🎯 Problem Statement

The National Cadet Corps (NCC) in India operates across **17 Directorates** and **837 Units** but lacks a unified digital system. Cadet data is fragmented across WhatsApp and paper records, leading to:
- Missed opportunities for cadet development
- Lack of transparency in performance tracking
- No institutional memory of achievements
- Inefficient manual reporting processes

## 💡 Solution

An AI-powered, role-based digital platform that:
- **Centralizes** cadet data across all NCC units
- **Analyzes** performance using AWS Bedrock AI
- **Recommends** personalized growth paths for cadets
- **Automates** report generation with GenAI
- **Preserves** institutional memory of events and achievements

## ✨ Key Features

### 1. Cadet Dashboard
- Real-time attendance tracking and visualization
- Camp completion history and progress
- Rank progression with milestone tracking
- Personalized AI-driven growth insights

### 2. AI Growth Intelligence Engine
- Analyzes cadet profiles using AWS Bedrock
- Recommends eligible camps (ATC, RDC, TSC, NIC)
- Identifies skill gaps with actionable improvement steps
- Predicts rank progression timeline

### 3. AI Report Assistant
- Generates structured camp reports automatically
- Creates event reflections using GenAI
- Allows review and editing before finalization
- Stores reports in cloud with easy access

### 4. Unit Activity Dashboard (Officers)
- Live participation statistics for entire unit
- Aggregate attendance and camp participation rates
- Individual cadet performance summaries
- Date range filtering for custom analytics

### 5. Institutional Memory Repository
- Searchable database of historical events
- Document storage and retrieval
- Relevance-based search ranking
- Unit and directorate filtering

## 🏗️ Technical Architecture

### Frontend
- **React.js 18+** with TypeScript
- **Tailwind CSS** for responsive design
- **Chart.js** for data visualizations
- Mobile-first responsive design

### Backend (Serverless)
- **AWS Lambda** (Node.js 18.x) for compute
- **API Gateway** for RESTful APIs
- **AWS Cognito** for authentication
- **DynamoDB** for NoSQL data storage
- **S3** for document storage
- **AWS Bedrock** (Claude 3 Sonnet) for AI capabilities

### Infrastructure
- **AWS CDK/Terraform** for Infrastructure as Code
- **CloudWatch** for logging and monitoring
- **IAM** for fine-grained access control

## 📊 System Architecture

```
┌─────────────────┐
│  React Web App  │
│  (Tailwind CSS) │
└────────┬────────┘
         │ HTTPS
         ▼
┌─────────────────┐
│  API Gateway    │
│  + Cognito Auth │
└────────┬────────┘
         │
    ┌────┴────┬────────┬──────────┬──────────┐
    ▼         ▼        ▼          ▼          ▼
┌────────┐ ┌──────┐ ┌─────┐ ┌─────────┐ ┌──────────┐
│ Auth   │ │Cadet │ │ AI  │ │ Report  │ │Analytics │
│Lambda  │ │Lambda│ │Lambda│ │ Lambda  │ │ Lambda   │
└───┬────┘ └──┬───┘ └──┬──┘ └────┬────┘ └─────┬────┘
    │         │        │         │            │
    ▼         ▼        ▼         ▼            ▼
┌─────────────────────────────────────────────────┐
│              DynamoDB Tables                     │
│  (Cadets, Attendance, Camps, Reports, Events)   │
└─────────────────────────────────────────────────┘
                      │
                      ▼
            ┌──────────────────┐
            │   AWS Bedrock    │
            │  (Claude 3 AI)   │
            └──────────────────┘
```

## 👥 User Roles

1. **Cadets**: Access personal dashboards, view AI recommendations, generate reports
2. **Officers**: Monitor unit activities, approve registrations, access analytics
3. **Admins**: Manage system configurations, approve user registrations

## 📋 Process Flow

```
Cadet Registration → Admin Approval → Secure Login → 
Role-Based Dashboard → AI-Driven Insights → Growth Tracking
```

## 🔒 Security Features

- AWS Cognito for secure authentication
- Role-based access control (RBAC)
- JWT token-based session management
- Encrypted data storage in DynamoDB
- Secure document storage in S3 with access controls

## 📱 Mobile Compatibility

- Fully responsive design for mobile devices
- Touch-friendly controls
- Optimized for 4G networks
- Adaptive layouts for different screen sizes

## 📈 Scalability

- **Serverless architecture** scales automatically
- **DynamoDB** handles high-throughput operations
- **Lambda functions** scale based on demand
- **Cost-optimized** with pay-per-use pricing

## 🧪 Testing Strategy

- **Unit Tests**: Specific examples and edge cases
- **Property-Based Tests**: 43 correctness properties using fast-check
- **Integration Tests**: End-to-end user flows
- **AWS Service Mocking**: For local development

## 📚 Documentation

- **[Requirements Document](requirements.md)**: 12 requirements with 60 acceptance criteria
- **[Design Document](design.md)**: Complete architecture, interfaces, and correctness properties
- **[Implementation Plan](tasks.md)**: 24 major tasks with 70+ sub-tasks

## 🚀 Getting Started

### Prerequisites
- Node.js 18.x or higher
- AWS Account with appropriate permissions
- AWS CLI configured
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/Priya0841/NayiSoch-NCC-Platform.git
cd NayiSoch-NCC-Platform

# Install dependencies (once implemented)
npm install

# Configure AWS credentials
aws configure

# Deploy infrastructure (once implemented)
npm run deploy
```

## 🎯 Project Status

**Current Phase**: Specification and Design Complete ✅

**Next Steps**:
1. Set up project structure and AWS infrastructure
2. Implement the authentication service
3. Build cadet management service
4. Integrate AI Growth Intelligence Engine
5. Develop React frontend

## 🤝 Contributing

This project is part of the NayiSoch hackathon submission. For questions or collaboration:
- GitHub: [@Priya0841](https://github.com/Priya0841)

## 📄 License

This project is developed for the  AI for Bharat hackathon.

## 🏆 Hackathon Submission

**Event**: AI for Bharat Hackathon  
**Category**: AI-Powered Solutions for Government/Defense  
**Team**: NayiSoch 
**Submission Date**: February 2026

---

**Built with ❤️ for India's National Cadet Corps**

