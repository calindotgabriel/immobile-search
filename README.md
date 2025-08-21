# 🏠 ImmoScout24 Search Platform

> **Real Estate Search Engine for Austria**
> 
> Handling **5,000+ daily searches** with reliable uptime

![ImmoScout24 Platform](https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=800&h=400&fit=crop&crop=entropy&auto=format&q=80)

## 🎯 What We Built

Property search platform with microservices architecture designed for Austria's real estate market. Our team built a hybrid AWS infrastructure combining serverless and traditional server components to handle thousands of daily searches efficiently.

**Key Features:**
- Distributed search service with geolocation filtering
- Multi-tenant authentication across microservices
- Event-driven architecture for real-time updates
- Auto-scaling search and user management services
- Cross-service communication with API Gateway

## 🏗️ Technical Architecture

**Frontend:** React 18, TypeScript, Tailwind CSS, React Query

**Microservices:** Node.js, Express, distributed across AWS Lambda and EC2

**Data Layer:** MongoDB (Atlas), Redis (ElastiCache), S3 for assets

**Infrastructure:** AWS API Gateway, Lambda, EC2, Application Load Balancer

## 🔧 Microservices Design

### Service Architecture
Our team designed independent microservices communicating through API Gateway and internal service mesh:

- **Search Service:** Handles property queries and filtering logic
- **User Service:** Authentication, authorization, and user management  
- **Property Service:** CRUD operations and property data management
- **Notification Service:** Real-time updates and email notifications
- **Analytics Service:** Search tracking and performance metrics

### Serverless + Server Hybrid
**Lambda Functions:** We implemented lightweight operations like image processing, notifications, and analytics
**EC2 Instances:** Heavy computational tasks like search indexing and database operations
**API Gateway:** Central routing and rate limiting across all services

### Inter-Service Communication
We implemented asynchronous messaging with SQS for non-critical operations and direct HTTP calls for real-time data. Each service maintains its own MongoDB collection while sharing common authentication tokens.

### Auto-Scaling Strategy
Lambda functions scale automatically based on demand. Our team configured EC2 instances with Application Load Balancer and auto-scaling groups that respond to CPU and memory metrics.

## 📊 Performance Characteristics

- **Service Independence:** Each microservice can be deployed and scaled separately
- **Fault Tolerance:** Service failures don't cascade due to circuit breaker patterns we implemented
- **Load Distribution:** Traffic automatically distributed across healthy instances
- **Cost Optimization:** Serverless functions reduce costs during low-traffic periods

## 🚀 Technical Challenges We Solved

### Service Discovery
Our team implemented service registry pattern where each microservice registers its health status and available endpoints with a central discovery service.

### Data Consistency
We used eventual consistency model with event sourcing for non-critical updates, while maintaining strong consistency for user authentication and payment-related operations through MongoDB transactions.

### Cross-Service Authentication
JWT tokens validated at API Gateway level, then passed to individual services with user context and permissions - a pattern we refined through team collaboration.

### Lambda Cold Start Optimization
We implemented connection pooling and provisioned concurrency for critical Lambda functions, reducing response times from 2s to 300ms during peak traffic.

### Monitoring & Observability
Our team set up distributed tracing across services using CloudWatch and custom metrics. Each service logs performance data that gets aggregated for system-wide monitoring.

## 🔗 Links

- **Portfolio:** [calingabriel.com](https://calingabriel.com)
- **Live Demo:** Coming soon

---

**💼 Available for similar projects** | **📧 calindotgabriel18@gmail.com** 
*Specializing in microservices architecture, AWS Lambda, and scalable distributed systems with MongoDB.*

