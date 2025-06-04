# Multivendor Marketplace - Django Project

A robust multivendor e-commerce platform built with Django that allows multiple sellers to list and sell their products through a single marketplace.

## Features

- **Multi-vendor Support**: Multiple sellers can register and manage their stores
- **Product Management**: Sellers can add, edit, and manage their products
- **Shopping Cart**: Users can add products to cart and manage their shopping
- **Order Management**: Complete order processing system
- **Payment Integration**: Stripe payment gateway integration
- **Email Notifications**: SendGrid integration for email communications
- **Responsive Design**: Mobile-friendly interface
- **Admin Dashboard**: Separate admin interfaces for marketplace admin and sellers

## Tech Stack

- **Backend**: Django 3.2.3
- **Database**: SQLite (Development) / PostgreSQL (Production-ready)
- **Payment Gateway**: Stripe
- **Email Service**: SendGrid
- **Frontend**: HTML, CSS, JavaScript
- **Image Processing**: Pillow

## Project Structure

```
multivendor-marketplace/
├── apps/
│   ├── cart/         # Shopping cart functionality
│   ├── multivendor/  # Core marketplace features
│   ├── order/        # Order management
│   ├── product/      # Product management
│   └── sellers/      # Seller management
├── galaxy/           # Main project configuration
├── static/          # Static files (CSS, JS, images)
├── media/           # User-uploaded files
└── requirements.txt # Project dependencies
```

## Prerequisites

- Python 3.6+
- pip (Python package manager)
- Virtual environment (recommended)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd multivendor-marketplace
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
- Create a `.env` file in the project root
- Add the following variables:
  ```
  # Django settings
  SECRET_KEY=your-secret-key-here
  DEBUG=True
  ALLOWED_HOSTS=localhost,127.0.0.1

  # Stripe settings
  STRIPE_PUB_KEY=your-stripe-public-key
  STRIPE_SECRET_KEY=your-stripe-secret-key

  # Email settings (SendGrid)
  EMAIL_HOST=smtp.sendgrid.net
  EMAIL_HOST_USER=apikey
  EMAIL_HOST_PASSWORD=your-sendgrid-api-key
  EMAIL_PORT=587
  EMAIL_USE_TLS=True
  DEFAULT_EMAIL_FROM=Galaxy <noreply@galaxy.com>
  ```
- Make sure to replace all placeholder values with your actual credentials
- Never commit the `.env` file to version control
- Keep your `.env` file secure and private

5. Run migrations:
```bash
python manage.py migrate
```

6. Create a superuser:
```bash
python manage.py createsuperuser
```

7. Run the development server:
```bash
python manage.py runserver
```

## Configuration

### Stripe Integration
1. Sign up for a Stripe account
2. Get your API keys from the Stripe dashboard
3. Update the `STRIPE_PUB_KEY` and `STRIPE_SECRET_KEY` in settings.py

### SendGrid Integration
1. Create a SendGrid account
2. Generate an API key
3. Update the `EMAIL_HOST_PASSWORD` in settings.py

## Usage

1. Access the admin interface at `/admin`
2. Create seller accounts through the admin panel
3. Sellers can access their dashboard at `/seller-admin`
4. Customers can browse products and make purchases

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the repository or contact the maintainers.

## Acknowledgments

- Django Documentation
- Stripe API Documentation
- SendGrid API Documentation 