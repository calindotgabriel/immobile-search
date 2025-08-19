# 🏠 ImmoScout24 Search Platform

> **Real Estate Search Engine for Austria**
> 
> Handling **5,000+ daily searches** with reliable uptime

![ImmoScout24 Platform](https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=800&h=400&fit=crop&crop=entropy&auto=format&q=80)

## 🎯 What I Built

Property search platform with geolocation filtering and user authentication for Austria's real estate market. The system handles thousands of daily searches while providing a smooth experience for agents, buyers, and landlords.

**Key Features:**
- Location-based property search with interactive maps
- Multi-user authentication (agents, buyers, landlords)
- Search result caching for better performance
- Mobile-responsive interface
- Property favorites and saved searches

## 🏗️ Technical Stack

**Frontend:** React 18, TypeScript, Tailwind CSS, Leaflet Maps, React Query

**Backend:** Node.js, Express, PostgreSQL with PostGIS, Redis, JWT Auth

**Infrastructure:** AWS (EC2, RDS, S3), CloudFront CDN

## 🔧 Technical Highlights

### Location Search
Used PostGIS for spatial queries and distance calculations. Learning curve was worth it for the performance on location-based searches.

### Caching Strategy
Added Redis caching for popular searches. Made a noticeable difference during peak hours when the same areas get searched frequently.

### Multi-User System
Implemented role-based authentication where agents can manage listings, buyers can save searches, and landlords handle portfolios.

### Map Integration
Integrated Leaflet with React for interactive property maps. Took some iterations to manage map state and property markers efficiently.

## 📊 Current Performance

- **~5,000** daily property searches
- **Multiple user types** with different permission levels
- **Good uptime** during peak usage periods
- **Responsive design** working well on mobile

## 🚀 What I Learned

- **PostGIS & Spatial Data:** Geographic queries and indexing
- **Caching Strategies:** When and how to cache search results
- **Multi-tenant Architecture:** Role-based permissions and access
- **Performance Optimization:** Database indexing and query optimization

## 🔗 Links

- **Portfolio:** [calingabriel.dev](https://calingabriel.dev)
- **Live Demo:** Coming soon

---

**💼 Available for similar projects** | **📧 calindotgabriel18@gmail.com** | **💰 €60-80/hour**

*Interested in building web applications with maps, search functionality, or multi-user systems.*
