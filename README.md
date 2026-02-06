# AquaGlow Booking API Documentation

![API](https://img.shields.io/badge/API-AquaGlow%20Booking-blue)
![Version](https://img.shields.io/badge/version-1.0.0-green)
![OpenAPI](https://img.shields.io/badge/OpenAPI-3.0.3-orange)
![License](https://img.shields.io/badge/license-MIT-brightgreen)

Professional API documentation for the AquaGlow Car Wash Booking System.
This repository hosts interactive API documentation using Redoc.

## 🌐 Live Documentation

Access the live documentation here:\
👉 https://stack-symphony.github.io/AQUAGLOW_API-docs/


## 📖 About

This documentation provides a complete reference for the AquaGlow
Booking API, which manages:

-   Car wash bookings and appointments
-   Customer registration and management
-   Service catalog with pricing
-   Payment processing
-   Time slot availability

## 🚀 Features

-   **Interactive API Console:** Try endpoints directly from the browser
-   **Complete Schema Documentation:** Request/response models with
    examples
-   **Search Functionality:** Quickly find endpoints
-   **Code Samples:** Available in multiple programming languages
-   **Responsive Design:** Works on desktop and mobile
-   **Dark/Light Mode:** Toggle between themes

## 📁 Repository Structure

    aquaglow-api-docs/
    ├── index.html              # Documentation viewer
    ├── openapi.yaml            # OpenAPI 3.0 specification
    ├── README.md               # This file
    └── .github/workflows/      # Deployment workflows (optional)

## 🔧 API Endpoints Overview

### Health Check

-   `GET /health` -- Check API status

### Authentication

-   `POST /api/auth/register` -- Register new user

### Bookings Management

-   `GET /api/bookings` -- Get all bookings (filter by date/service)
-   `POST /api/bookings` -- Create new booking
-   `GET /api/bookings/{id}` -- Get specific booking
-   `PATCH /api/bookings/{id}` -- Update booking time slot
-   `GET /api/bookings/available-slots` -- Check availability

### Services

-   `GET /api/services` -- List all car wash services

### Customers

-   `GET /api/customers` -- Get customer list

## 🛠️ Local Development

### View Documentation Locally

Clone the repository:

``` bash
git clone https://github.com/yourusername/aquaglow-api-docs.git
cd aquaglow-api-docs
```

Open in browser:

``` bash
# Using Python
python -m http.server 8000
# Then visit http://localhost:8000

# Or using Node.js
npx serve .
```

### Update Documentation

Edit the OpenAPI specification:

``` bash
nano openapi.yaml
# or
code openapi.yaml
```

Validate your changes:

``` bash
# Install OpenAPI validator
npm install -g @apidevtools/swagger-cli

# Validate the spec
swagger-cli validate openapi.yaml
```

Test locally then push:

``` bash
git add .
git commit -m "Updated API documentation"
git push origin main
```

## 🌍 Deployment

### GitHub Pages Setup

1.  Go to repository **Settings**
2.  Click **Pages** in the sidebar
3.  Under **Source**, select:
    -   **Branch:** main (or master)
    -   **Folder:** / (root)
4.  Click **Save**
5.  Wait a few minutes for deployment

Your docs will be live at:\
`https://[username].github.io/aquaglow-api-docs/`

### Custom Domain (Optional)

To use `docs.aquaglow.example.com`:

Add CNAME file:

``` bash
echo "docs.aquaglow.example.com" > CNAME
```

Update DNS records at your domain registrar:

    Type: CNAME
    Name: docs
    Value: yourusername.github.io

In GitHub Pages settings, add your custom domain.

## 📊 API Response Format

All API responses follow this structure:

``` json
{
  "success": true,
  "data": { },
  "message": "Optional message"
}
```

## 🎨 Styling Customization

To customize the documentation appearance, edit the `index.html` file:

``` javascript
Redoc.init('openapi.yaml', {
  theme: {
    colors: {
      primary: { main: '#3f51b5' },
      success: { main: '#4caf50' },
      warning: { main: '#ff9800' },
      error: { main: '#f44336' }
    },
    typography: {
      fontSize: '16px',
      fontFamily: 'Roboto, Arial, sans-serif'
    }
  }
});
```

## 🔗 Useful Links

-   OpenAPI Specification: https://spec.openapis.org/oas/v3.0.3
-   Redoc Documentation: https://github.com/Redocly/redoc
-   Swagger Editor: https://editor.swagger.io/
-   GitHub Pages: https://pages.github.com/

## 📝 License

This documentation is licensed under the MIT License. See the `LICENSE`
file for details.

## 🤝 Contributing

1.  Fork the repository
2.  Create a feature branch (`git checkout -b feature/improvement`)
3.  Commit changes (`git commit -m 'Add some feature'`)
4.  Push to branch (`git push origin feature/improvement`)
5.  Open a Pull Request

## 📞 Support

For API support or questions:

-   Email: support@aquaglow.example.com
-   Issues: GitHub Issues
-   Documentation Updates: Edit the `openapi.yaml` file

├── README.md               # This file
└── .github/workflows/      # Deployment workflows (optional)
