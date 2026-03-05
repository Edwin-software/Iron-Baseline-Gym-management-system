# GymFlow Pro - Comprehensive Gym Management System

A full-featured, multi-role gym management platform designed to streamline operations, member management, trainer coordination, and financial tracking. Built with modern web technologies and designed for scalability, security, and ease of use.

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [User Roles & Access Levels](#user-roles--access-levels)
- [Technology Stack](#technology-stack)
- [Installation & Setup](#installation--setup)
- [Configuration](#configuration)
- [Database Schema](#database-schema)
- [API Endpoints](#api-endpoints)
- [User Dashboards](#user-dashboards)
- [Features by Role](#features-by-role)
- [Security Features](#security-features)
- [Deployment Guide](#deployment-guide)
- [Development Guidelines](#development-guidelines)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Project Overview

**GymFlow Pro** is an enterprise-grade gym management system that consolidates all gym operations into a single, intuitive platform. It serves as the central hub for:

- **Gym Owners/Administrators**: System oversight, user management, financial analytics, and reporting
- **Managers**: Member management, session verification, staff coordination
- **Trainers**: Client management, workout planning, session scheduling, progress tracking
- **Trainees/Members**: Membership tracking, booking sessions, viewing workout plans, purchasing products
- **Accounts Staff**: Financial management, expense tracking, income recording, salary management

The system is built with responsive design principles, ensuring seamless operation across desktop and mobile devices.

---

## ✨ Key Features

### 📊 Dashboard & Analytics
- **Real-time statistics**: Member counts, active sessions, revenue metrics
- **Interactive charts**: Fitness progress tracking, revenue trends, membership distribution
- **Customizable widgets**: Role-specific dashboard configurations
- **Notifications**: Real-time alerts for pending actions and important updates

### 👥 Member Management
- **Comprehensive member profiles**: Complete personal and fitness information
- **Membership plans**: Multiple tier options with flexible durations
- **Membership tracking**: Active, expired, and pending membership status
- **Member history**: Track membership changes and renewal dates

### 💪 Training Management
- **Session scheduling**: Calendar-based booking system
- **Trainer assignment**: Flexible trainer allocation based on specialization
- **Workout plans**: Pre-designed and customizable workout programs
- **Progress tracking**: Detailed client progress metrics and analytics
- **Session verification**: Manager approval workflow for sessions

### 💰 Financial Management
- **Income tracking**: Record all revenue sources
- **Expense management**: Categorized expense tracking
- **Transaction history**: Complete audit trail of all financial activities
- **Reports**: Generate comprehensive financial reports (PDF export)
- **Salary management**: Employee salary calculation and deduction tracking

### 📦 Product Management
- **Product catalog**: Manage supplements, gear, and merchandise
- **Inventory system**: Track product stock levels
- **Purchase history**: Record member purchases
- **Pricing management**: Dynamic pricing and promotional pricing

### 🔐 Authentication & Security
- **Multi-role authentication**: Role-based login system
- **Secure password handling**: Password strength validation
- **Session management**: Secure session tokens and expiration
- **Activity logging**: Track all user actions for security auditing
- **Google OAuth integration**: Simplified signup with Google accounts

### 📱 Responsive Design
- **Mobile-first approach**: Optimized for all screen sizes
- **Progressive Web App**: Mobile app-like experience
- **Touch-friendly interface**: Optimized controls for mobile devices
- **Cross-browser compatibility**: Works on all modern browsers

### 📈 Reporting & Export
- **PDF reports**: Export financial reports and member lists
- **Data analytics**: Comprehensive business intelligence
- **Custom reports**: Generate reports based on specific criteria
- **Data export**: Export data for external analysis

---

## 🏗 System Architecture

```
GymFlow Pro
│
├── Frontend (HTML5, CSS3, JavaScript)
│   ├── Authentication Hub
│   ├── Admin Dashboard
│   ├── Manager Dashboard
│   ├── Trainer Dashboard
│   ├── Trainee Portal
│   └── Accounts Dashboard
│
├── Backend (Node.js / Express.js - Optional)
│   ├── Authentication Service
│   ├── User Management
│   ├── Member Management
│   ├── Session Management
│   ├── Financial Management
│   └── Reporting Service
│
├── Database (Supabase / PostgreSQL)
│   ├── Users Table
│   ├── Members Table
│   ├── Memberships Table
│   ├── Training Sessions Table
│   ├── Workouts Table
│   ├── Financial Records Table
│   ├── Products Table
│   └── Transactions Table
│
└── External Services
    ├── Google OAuth
    ├── Supabase Auth
    └── PDF Generation (jsPDF)
```

---

## 👥 User Roles & Access Levels

### 1. **Owner**
- **Access Level**: Full system access
- **Responsibilities**: 
  - Overall system management
  - Business strategy and planning
  - Financial oversight
  - User and privilege management
  - System configuration

### 2. **Admin**
- **Access Level**: System-wide administrative access
- **Responsibilities**:
  - System maintenance
  - User account management
  - Privilege assignment
  - Data security
  - Backup and recovery

### 3. **Manager**
- **Access Level**: Operational management
- **Responsibilities**:
  - Member verification and management
  - Session verification and approval
  - Staff coordination
  - Basic financial tracking
  - Reporting to administration

### 4. **Trainer**
- **Access Level**: Client and session management
- **Responsibilities**:
  - Client management
  - Workout plan creation and updates
  - Session scheduling
  - Progress tracking
  - Client communication

### 5. **Trainee/Member**
- **Access Level**: Personal account access
- **Responsibilities**:
  - View personal membership
  - Book training sessions
  - Track progress
  - Purchase products
  - Manage profile

### 6. **Accounts Staff**
- **Access Level**: Financial management
- **Responsibilities**:
  - Income recording
  - Expense tracking
  - Salary management
  - Financial reporting
  - Transaction verification

---

## 🛠 Technology Stack

### Frontend
- **HTML5**: Semantic markup and structure
- **CSS3**: Modern styling with custom properties (CSS Variables)
- **JavaScript (ES6+)**: Interactive functionality
- **Font Awesome**: Icon library
- **Chart.js**: Data visualization
- **jsPDF**: PDF generation and export

### Backend (Recommended for Production)
- **Node.js**: Runtime environment
- **Express.js**: Web framework
- **Supabase/PostgreSQL**: Database
- **JSON Web Tokens (JWT)**: Authentication
- **bcryptjs**: Password hashing

### External Services
- **Supabase**: Authentication and database hosting
- **Google OAuth 2.0**: Social authentication
- **HTML2Canvas**: Screenshot/PDF export
- **jsPDF**: PDF document generation

### Development Tools
- **Git**: Version control
- **VS Code**: Code editor (recommended)
- **npm/pnpm**: Package management
- **Chrome DevTools**: Debugging and development

---

## 📦 Installation & Setup

### Prerequisites
- Node.js (v14+ recommended)
- npm or pnpm package manager
- Modern web browser
- Supabase account (for backend setup)
- Google OAuth credentials (for social login)

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/gymflow-pro.git
cd gymflow-pro
```

### Step 2: Install Dependencies
```bash
npm install
# or
pnpm install
```

### Step 3: Set Up Environment Variables

Create a `.env.local` file in the project root:

```env
# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_anon_key_here

# Google OAuth (Optional)
NEXT_PUBLIC_GOOGLE_CLIENT_ID=your_google_client_id_here

# API Configuration
NEXT_PUBLIC_API_URL=http://localhost:3000/api

# Environment
NODE_ENV=development
```

### Step 4: Initialize Database

If using Supabase:
```bash
npx supabase db push
```

### Step 5: Start Development Server
```bash
npm run dev
# or
pnpm dev
```

The application will be available at `http://localhost:3000`

---

## ⚙️ Configuration

### Supabase Setup

1. **Create Supabase Project**:
   - Go to [supabase.com](https://supabase.com)
   - Create a new project
   - Set up PostgreSQL database

2. **Configure Authentication**:
   - Enable Email/Password auth
   - Configure Google OAuth provider
   - Set up auth redirect URLs

3. **Create Database Tables**:
   Use the SQL migrations provided in `/scripts/database` directory

### Google OAuth Configuration

1. **Create Google Cloud Project**:
   - Visit [Google Cloud Console](https://console.cloud.google.com)
   - Create new project
   - Enable Google+ API

2. **Create OAuth Credentials**:
   - Go to Credentials section
   - Create OAuth 2.0 Client ID
   - Set authorized redirect URIs

3. **Update Configuration**:
   - Copy Client ID to `.env.local`
   - Configure in Supabase OAuth providers

### Custom Branding

Edit `public/config.js` to customize:
```javascript
const CONFIG = {
  appName: 'GymFlow Pro',
  primaryColor: '#2a5bd7',
  secondaryColor: '#10b981',
  logo: '/images/logo.png',
  currency: 'KSh',
  timezone: 'Africa/Nairobi'
};
```

---

## 🗄 Database Schema

### Core Tables

#### Users Table
```sql
CREATE TABLE users (
  id UUID PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  full_name VARCHAR(255) NOT NULL,
  role ENUM('owner', 'admin', 'manager', 'trainer', 'trainee', 'accounts'),
  password_hash VARCHAR(255),
  avatar_url VARCHAR(255),
  phone VARCHAR(20),
  is_active BOOLEAN DEFAULT true,
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);
```

#### Members Table
```sql
CREATE TABLE members (
  id UUID PRIMARY KEY,
  user_id UUID REFERENCES users(id),
  date_of_birth DATE,
  gender ENUM('male', 'female', 'other'),
  height DECIMAL(5,2),
  weight DECIMAL(6,2),
  emergency_contact VARCHAR(255),
  membership_status ENUM('active', 'inactive', 'expired', 'suspended'),
  joined_date DATE DEFAULT TODAY(),
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Memberships Table
```sql
CREATE TABLE memberships (
  id UUID PRIMARY KEY,
  member_id UUID REFERENCES members(id),
  plan_name VARCHAR(100),
  price DECIMAL(10,2),
  duration_days INT,
  start_date DATE,
  end_date DATE,
  status ENUM('active', 'expired', 'paused'),
  auto_renew BOOLEAN DEFAULT false,
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Training Sessions Table
```sql
CREATE TABLE training_sessions (
  id UUID PRIMARY KEY,
  trainer_id UUID REFERENCES users(id),
  member_id UUID REFERENCES members(id),
  session_date DATE,
  start_time TIME,
  end_time TIME,
  session_type VARCHAR(50),
  status ENUM('scheduled', 'completed', 'cancelled', 'no-show'),
  notes TEXT,
  created_at TIMESTAMP DEFAULT NOW()
);
```

#### Financial Records Table
```sql
CREATE TABLE financial_records (
  id UUID PRIMARY KEY,
  record_type ENUM('income', 'expense'),
  amount DECIMAL(10,2),
  category VARCHAR(100),
  description TEXT,
  recorded_by UUID REFERENCES users(id),
  record_date DATE,
  status ENUM('pending', 'verified', 'rejected'),
  created_at TIMESTAMP DEFAULT NOW()
);
```

---

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/signup` - Create new account
- `POST /api/auth/logout` - User logout
- `POST /api/auth/refresh` - Refresh JWT token
- `POST /api/auth/forgot-password` - Password reset request

### Members
- `GET /api/members` - List all members
- `GET /api/members/:id` - Get member details
- `POST /api/members` - Create new member
- `PUT /api/members/:id` - Update member info
- `DELETE /api/members/:id` - Delete member

### Memberships
- `GET /api/memberships` - List memberships
- `POST /api/memberships` - Create membership
- `PUT /api/memberships/:id` - Update membership
- `GET /api/memberships/active` - Get active memberships only

### Training Sessions
- `GET /api/sessions` - List all sessions
- `POST /api/sessions` - Create new session
- `PUT /api/sessions/:id` - Update session
- `DELETE /api/sessions/:id` - Cancel session
- `POST /api/sessions/:id/verify` - Manager verification

### Financial Records
- `GET /api/financial/records` - List financial records
- `POST /api/financial/income` - Record income
- `POST /api/financial/expense` - Record expense
- `GET /api/financial/reports` - Generate financial reports

### Products
- `GET /api/products` - List products
- `POST /api/products` - Create product
- `PUT /api/products/:id` - Update product
- `DELETE /api/products/:id` - Delete product

---

## 📱 User Dashboards

### Admin Dashboard
**Location**: `/admin`

**Features**:
- System overview and KPIs
- User account management
- Member verification
- Training session oversight
- Financial reports
- User privilege management
- System settings

**Key Sections**:
- Dashboard Overview (stats and charts)
- User Accounts (CRUD operations)
- Current Members
- Valid Memberships
- Training Sessions
- Session Verification
- Product Management
- User Privileges

### Manager Dashboard
**Location**: `/manager`

**Features**:
- Operational overview
- Member management
- Session verification workflow
- Staff coordination
- Performance analytics
- Task management

**Key Sections**:
- Dashboard (stats and charts)
- Members Management
- Session Verification
- Reports
- Notifications

### Trainer Dashboard
**Location**: `/trainer`

**Features**:
- Client management
- Session scheduling
- Workout planning
- Progress tracking
- Client messaging
- Performance analytics

**Key Sections**:
- Home (today's overview)
- Clients (manage trainee list)
- Workouts (create and modify plans)
- Schedule (session calendar)
- Messages (client communication)
- Progress (client metrics)

### Trainee Dashboard
**Location**: `/trainee`

**Features**:
- Membership information
- Session booking
- Workout tracking
- Progress visualization
- Product shopping
- Profile management

**Key Sections**:
- Membership Overview
- Booking Sessions
- My Workouts
- Progress Charts
- Products
- Trainer Information

### Accounts Dashboard
**Location**: `/accounts`

**Features**:
- Income tracking
- Expense management
- Salary calculations
- Financial reporting
- Transaction audit
- Financial analytics

**Key Sections**:
- Dashboard (financial overview)
- Membership Plans
- Trainees (payment tracking)
- Employees & Salaries
- Record Income
- Record Expenses
- Transactions
- Financial Reports
- Settings

---

## 🎯 Features by Role

### Owner/Admin
✅ Complete system access  
✅ User and privilege management  
✅ Financial oversight  
✅ System configuration  
✅ Backup and recovery  
✅ Comprehensive reporting  
✅ Audit trails  
✅ API key management  

### Manager
✅ Member verification  
✅ Session approval  
✅ Staff coordination  
✅ Performance reports  
✅ Member communications  
✅ Basic financial tracking  
✅ Activity monitoring  

### Trainer
✅ Client management  
✅ Workout plan creation  
✅ Session scheduling  
✅ Progress tracking  
✅ Client communication  
✅ Performance metrics  
✅ Assessment tools  

### Trainee/Member
✅ Membership viewing  
✅ Session booking  
✅ Workout tracking  
✅ Progress viewing  
✅ Product purchase  
✅ Profile management  
✅ Schedule viewing  

### Accounts Staff
✅ Income recording  
✅ Expense tracking  
✅ Salary management  
✅ Financial reporting  
✅ Transaction auditing  
✅ PDF export  
✅ Data analysis  

---

## 🔐 Security Features

### Authentication & Authorization
- **JWT-based authentication**: Secure token-based sessions
- **Role-based access control (RBAC)**: Fine-grained permission management
- **Password hashing**: bcryptjs with salt rounds
- **Session management**: Automatic expiration and refresh tokens
- **Multi-factor authentication**: Optional 2FA support

### Data Protection
- **SSL/TLS encryption**: Secure data transmission
- **Database encryption**: Encrypted sensitive fields
- **Input validation**: XSS and SQL injection prevention
- **CSRF protection**: Cross-site request forgery prevention
- **Rate limiting**: Prevent brute force attacks

### Compliance & Auditing
- **Activity logging**: All user actions tracked
- **Audit trails**: Complete operation history
- **Data privacy**: GDPR-compliant data handling
- **Compliance reports**: Generate compliance documentation

### Security Best Practices
- No hardcoded credentials in code
- Environment variable configuration
- Regular security updates
- Secure dependency management
- Security headers configuration

---

## 🚀 Deployment Guide

### Deploy to Vercel (Recommended)

1. **Push to GitHub**:
```bash
git push origin main
```

2. **Connect to Vercel**:
   - Visit [vercel.com](https://vercel.com)
   - Import GitHub repository
   - Configure environment variables
   - Deploy

3. **Configure Custom Domain**:
   - Add custom domain in Vercel settings
   - Configure DNS records

### Deploy to Other Platforms

#### Heroku
```bash
heroku create gymflow-pro
heroku addons:create heroku-postgresql:standard-0
git push heroku main
```

#### Docker Deployment
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package.json .
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

Build and run:
```bash
docker build -t gymflow-pro .
docker run -p 3000:3000 gymflow-pro
```

### Environment Setup for Production
```env
NODE_ENV=production
NEXT_PUBLIC_SUPABASE_URL=https://prod-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=production_key_here
JWT_SECRET=your_jwt_secret_here
DATABASE_URL=postgresql://user:pass@host/dbname
```

---

## 🛠 Development Guidelines

### Code Structure
```
gymflow-pro/
├── public/
│   ├── index.html
│   ├── styles/
│   │   ├── global.css
│   │   └── variables.css
│   ├── images/
│   └── js/
│       ├── auth.js
│       ├── dashboard.js
│       └── utils.js
├── src/
│   ├── components/
│   ├── pages/
│   ├── lib/
│   └── utils/
├── scripts/
│   └── database/
│       ├── init.sql
│       └── migrations/
├── .env.local
├── package.json
└── README.md
```

### Development Standards
- **Code Style**: Follow ESLint configuration
- **Comments**: Document complex logic
- **Testing**: Write unit tests for functions
- **Git Commits**: Use conventional commit messages
- **Pull Requests**: Include description and testing notes

### Common Commands
```bash
# Development
npm run dev              # Start dev server
npm run build            # Build for production
npm start                # Start production server

# Testing
npm test                 # Run tests
npm run test:watch      # Watch mode testing

# Linting
npm run lint             # Run ESLint
npm run lint:fix         # Fix linting issues

# Database
npm run db:push          # Push schema changes
npm run db:reset         # Reset database
```

---

## 🐛 Troubleshooting

### Common Issues

#### 1. Supabase Connection Error
**Problem**: Cannot connect to Supabase database

**Solution**:
- Verify `.env.local` credentials
- Check network connectivity
- Confirm Supabase project is active
- Review Supabase dashboard for errors

#### 2. Authentication Failures
**Problem**: Users unable to login

**Solution**:
- Clear browser cache and cookies
- Verify email/password combination
- Check user account status in database
- Review auth logs in Supabase

#### 3. Session Expiration
**Problem**: Sessions expiring too quickly

**Solution**:
- Increase JWT expiration time in config
- Check token refresh mechanism
- Verify system time synchronization
- Review session storage

#### 4. Performance Issues
**Problem**: Dashboard loading slowly

**Solution**:
- Optimize database queries
- Implement pagination for large datasets
- Cache frequently accessed data
- Use CDN for static assets
- Review and optimize images

#### 5. Mobile Responsiveness Issues
**Problem**: Layout breaks on mobile devices

**Solution**:
- Test on multiple device sizes
- Check CSS media queries
- Verify viewport settings
- Test touch interactions
- Use Chrome DevTools device emulation

### Debug Mode
Enable debug logging:
```javascript
localStorage.setItem('debug', 'true');
```

Check browser console for detailed logs.

---

## 📞 Support & Documentation

### Resources
- **Supabase Docs**: https://supabase.com/docs
- **Chart.js Docs**: https://www.chartjs.org/docs
- **Font Awesome**: https://fontawesome.com/search
- **MDN Web Docs**: https://developer.mozilla.org

### Getting Help
1. Check this README for answers
2. Search GitHub issues
3. Review Supabase documentation
4. Contact development team

### Reporting Bugs
Create an issue with:
- Detailed description
- Steps to reproduce
- Expected vs. actual behavior
- Screenshots/error logs
- Browser and OS information

---

## 🤝 Contributing

### How to Contribute
1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

### Development Workflow
1. Create issue for discussion
2. Assign yourself
3. Create feature branch from issue
4. Make changes and test thoroughly
5. Submit PR with description
6. Await review and merge

---

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

---

## 👨‍💼 Project Information

**Project Name**: GymFlow Pro  
**Version**: 1.0.0  
**Release Date**: 2024  
**Maintainer**: Development Team  

---

## 🎓 Additional Resources

### Tutorials & Guides
- [Getting Started with Gym Dashboard](docs/getting-started.md)
- [User Role Management](docs/roles.md)
- [Financial Management Guide](docs/financial.md)
- [Trainer Setup Guide](docs/trainer-setup.md)
- [API Documentation](docs/api.md)

### Video Tutorials
- Dashboard Overview
- Member Management
- Session Scheduling
- Financial Reporting

---

## ✅ Checklist for New Installations

Before going live:

- [ ] Environment variables configured
- [ ] Database migrations run successfully
- [ ] Supabase auth configured
- [ ] Google OAuth setup complete
- [ ] SSL certificate installed
- [ ] Backup strategy implemented
- [ ] Admin accounts created
- [ ] Security audit completed
- [ ] Performance testing done
- [ ] User documentation prepared
- [ ] Staff training completed
- [ ] Monitoring and alerting setup

---

## 📊 Version History

### v1.0.0 (Initial Release)
- Core gym management functionality
- Multi-role user system
- Member management
- Session scheduling
- Financial tracking
- Product management
- Reporting system

---

## 🙌 Acknowledgments

- Built with modern web technologies
- Supabase for reliable backend infrastructure
- Font Awesome for beautiful icons
- Chart.js for data visualization
- Open source community contributors

---

**For more information, visit the project repository or contact the development team.**

Last Updated: January 2024  
Documentation Version: 1.0
