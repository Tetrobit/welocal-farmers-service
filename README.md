# WeLocal Farmers Service

Agricultural and farming management service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Payment Processing**: Stripe
- **Weather API**: OpenWeatherMap
- **Maps Integration**: Google Maps API
- **IoT Integration**: MQTT

## Features

- Farm profile management
- Crop management and tracking
- Weather monitoring and alerts
- Equipment management
- Supply chain tracking
- Harvest scheduling
- Market price tracking
- Direct sales platform
- Farm analytics
- Resource planning
- IoT device integration
- Seasonal planning

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- Stripe account
- OpenWeatherMap API key
- Google Maps API key
- MQTT broker

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-farmers-service.git
   cd welocal-farmers-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8084
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   OPENWEATHERMAP_API_KEY=your-openweathermap-api-key
   GOOGLE_MAPS_API_KEY=your-google-maps-api-key
   MQTT_BROKER_URL=your-mqtt-broker-url
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-farmers-service .
docker run -p 8084:8084 welocal-farmers-service
```

## API Endpoints

### Farm Management
- `GET /api/v1/farms` - Get farms list
- `POST /api/v1/farms` - Create farm profile
- `GET /api/v1/farms/:id` - Get farm details
- `PUT /api/v1/farms/:id` - Update farm profile
- `DELETE /api/v1/farms/:id` - Delete farm profile

### Crop Management
- `GET /api/v1/farms/:id/crops` - Get farm crops
- `POST /api/v1/farms/:id/crops` - Add crop
- `PUT /api/v1/crops/:id` - Update crop details
- `DELETE /api/v1/crops/:id` - Delete crop
- `GET /api/v1/crops/:id/history` - Get crop history

### Weather Monitoring
- `GET /api/v1/farms/:id/weather` - Get farm weather
- `GET /api/v1/farms/:id/weather/forecast` - Get weather forecast
- `POST /api/v1/farms/:id/weather/alerts` - Set up weather alerts

### Equipment Management
- `GET /api/v1/farms/:id/equipment` - Get farm equipment
- `POST /api/v1/farms/:id/equipment` - Add equipment
- `PUT /api/v1/equipment/:id` - Update equipment status
- `GET /api/v1/equipment/:id/maintenance` - Get maintenance history

### Market Prices
- `GET /api/v1/market/prices` - Get market prices
- `GET /api/v1/market/prices/:crop` - Get specific crop prices
- `POST /api/v1/market/listings` - Create market listing
- `GET /api/v1/market/listings` - Get market listings

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── payments/        # Payment processing
├── weather/         # Weather monitoring
├── maps/            # Maps integration
├── iot/             # IoT device integration
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure payment processing
- IoT device authentication

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 