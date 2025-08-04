# Space Flow - Co-working Space Management System

A modern Django-based web application for managing coworking spaces, including desk bookings, meeting room reservations, membership management, and office leasing.

## 🚀 Features

- **User Management**: Registration, authentication, and role-based access control
- **Resource Booking**: Book desks, meeting rooms, and offices with real-time availability
- **Membership Plans**: Flexible subscription plans with different access levels
- **Lease Management**: Long-term office leasing with contract management
- **Admin Dashboard**: Comprehensive admin interface for staff and administrators
- **Modern UI**: Responsive design with Tailwind CSS and Alpine.js

## 🛠️ Technology Stack

- **Backend**: Django 5.2.4
- **Database**: SQLite (development)
- **Frontend**: Tailwind CSS
- **Python**: 3.12+
- **Package Manager**: uv

## 📋 Prerequisites

- Python 3.12 or higher
- uv package manager (recommended) or pip
- Git

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Solvit-Africa-Training-Center/didier_repo_learn.git
cd didier_repo_learn
```

### 2. Set Up Virtual Environment

Using uv (recommended):
```bash
uv sync
```

Or using pip:
```bash
uv venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
uv add -r requirements.txt
```

### 3. Environment Configuration

Create a `.env` file in the project root:

Edit `.env` with your configuration:
```env
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3
ALLOWED_HOSTS=localhost,127.0.0.1
```

### 4. Database Setup

```bash
uv run manage.py migrate
```

### 5. Create Superuser

```bash
uv run  manage.py createsuperuser
```

### 6. Run the Development Server

```bash
uv run manage.py runserver
```

Visit [http://127.0.0.1:8000](http://127.0.0.1:8000) to access the application.

## 📁 Project Structure

```
co-work_connect/
├── main_app/                 # Django project settings
│   ├── settings.py          # Main settings file
│   ├── urls.py              # Main URL configuration
│   └── wsgi.py              # WSGI configuration
├── core_app/                # Main application
│   ├── models.py            # Database models
│   ├── views.py             # View functions
│   ├── forms.py             # Form definitions
│   ├── admin.py             # Admin interface
│   ├── permissions.py       # Custom permissions
│   ├── templates/           # HTML templates
│   └── static/              # Static files
├── media/                   # User uploaded files
├── manage.py                # Django management script
├── pyproject.toml           # Project dependencies
└── README.md               # This file
```

## 🗄️ Database Models

### Core Models

- **UserProfile**: Extended user information with roles and preferences
- **Resource**: Desks, meeting rooms, and offices with availability tracking
- **Booking**: Time-based resource reservations
- **LeaseContract**: Long-term office leases
- **MembershipPlan**: Subscription plans with different access levels
- **Subscription**: User membership subscriptions

### User Roles

- **Member**: Basic user with booking capabilities
- **Staff**: Can manage bookings and resources
- **Admin**: Full administrative access

## 🔧 Configuration

### Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `DEBUG` | Debug mode | `True` |
| `DATABASE_URL` | Database connection string | `sqlite:///db.sqlite3` |
| `ALLOWED_HOSTS` | Allowed hostnames | `localhost,127.0.0.1` |

### Settings Customization

Key settings can be modified in `main_app/settings.py`:

- Database configuration
- Static and media file paths
- Authentication settings
- Email configuration
- Security settings



## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:

- Create an issue in the GitHub repository
- Review the Django documentation for framework-specific questions

## 🔄 Version History

- **v0.1.0**: Initial release with basic booking and user management
- **v0.2.0**: Added membership plans and subscription management
- **v0.3.0**: Enhanced admin interface and reporting features

## 🙏 Acknowledgments

- Django community for the excellent framework
- Tailwind CSS for the beautiful UI components
