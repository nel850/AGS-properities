# AGS Properties

A comprehensive property listing management software designed to streamline real estate operations for agents, brokers, and property management companies.

## Features

- **Property Listings Management**: Create, edit, and manage property listings with detailed information
- **Advanced Search & Filtering**: Powerful search functionality with multiple filter options
- **Client Management**: Maintain client profiles, preferences, and interaction history
- **Document Management**: Upload and organize property documents, contracts, and media
- **Lead Tracking**: Track inquiries and manage potential buyers/tenants
- **Reporting & Analytics**: Generate reports on listings, sales, and market trends
- **Mobile Responsive**: Access your listings on any device
- **Multi-user Support**: Role-based access for different team members

## Installation

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Database (PostgreSQL/MySQL/MongoDB)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/nel850/ags-properties.git
   cd ags-properties
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the root directory:
   ```env
   DATABASE_URL=your_database_connection_string
   JWT_SECRET=your_jwt_secret_key
   UPLOAD_PATH=./uploads
   PORT=3000
   ```

4. **Database Setup**
   ```bash
   npm run migrate
   npm run seed
   ```

5. **Start the application**
   ```bash
   # Development mode
   npm run dev

   # Production mode
   npm run build
   npm start
   ```

## Usage

### Getting Started

1. **Admin Setup**: Create your first admin account at `/setup`
2. **Add Properties**: Navigate to the dashboard and click "Add New Property"
3. **Manage Listings**: Use the listings page to view, edit, and organize properties
4. **Client Portal**: Share property links with clients for viewing

### Key Workflows

#### Adding a New Property
1. Go to Dashboard → Add Property
2. Fill in property details (location, price, features)
3. Upload photos and documents
4. Set visibility and availability status
5. Publish listing

#### Managing Inquiries
1. View inquiries in the Leads section
2. Respond to client messages
3. Schedule property viewings
4. Track interaction history

## API Documentation

The software provides a RESTful API for integration with third-party services.

### Authentication
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password"
}
```

### Property Endpoints
```http
GET /api/properties          # Get all properties
GET /api/properties/:id      # Get specific property
POST /api/properties         # Create new property
PUT /api/properties/:id      # Update property
DELETE /api/properties/:id   # Delete property
```

For complete API documentation, visit `/api/docs` when running the application.

## Configuration

### User Roles

- **Super Admin**: Full system access
- **Admin**: Manage properties and users
- **Agent**: Manage assigned properties
- **Viewer**: Read-only access

### Customization

The software supports customization through:
- Custom fields for properties
- Branding and theme options
- Email templates
- Report formats

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

### Development Guidelines

- Follow existing code style and conventions
- Write unit tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## Testing

```bash
# Run all tests
npm test

# Run tests with coverage
npm run test:coverage

# Run specific test suite
npm run test:unit
npm run test:integration
```

## Deployment

### Production Deployment

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Set production environment variables**
   ```bash
   NODE_ENV=production
   DATABASE_URL=production_database_url
   ```

3. **Deploy using PM2 (recommended)**
   ```bash
   npm install -g pm2
   pm2 start ecosystem.config.js
   ```

### Docker Deployment

```bash
# Build Docker image
docker build -t ags-properties .

# Run container
docker run -p 3000:3000 -e DATABASE_URL=your_db_url ags-properties
```

## Support

### Documentation
- User Guide: `/docs/user-guide.md`
- Developer Guide: `/docs/developer-guide.md`
- FAQ: `/docs/faq.md`

### Getting Help
- Create an issue on GitHub for bugs
- Join our community forum for discussions
- Email support: support@agsproperties.com

### System Requirements

**Minimum Requirements:**
- 2GB RAM
- 10GB storage space
- Modern web browser (Chrome, Firefox, Safari, Edge)

**Recommended:**
- 4GB RAM
- 50GB storage space
- High-speed internet connection

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Changelog

### Version 2.1.0 (Latest)
- Added advanced search filters
- Improved mobile responsiveness
- New reporting dashboard
- Bug fixes and performance improvements

### Version 2.0.0
- Major UI/UX redesign
- API v2 implementation
- Multi-language support
- Enhanced security features

See [CHANGELOG.md](CHANGELOG.md) for complete version history.

## Contact

**AGS Properties Development Team**
- Website: https://www.agsproperties.com
- Email: info@agsproperties.com
- GitHub: https://github.com/agsproperties
- LinkedIn: https://linkedin.com/company/ags-properties

---

⭐ If you find this software helpful, please consider giving us a star on GitHub!