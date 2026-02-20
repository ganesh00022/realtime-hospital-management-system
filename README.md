# realtime-hospital-management-system
Real-time hospital resource monitoring system for NHM to manage OPD appointments, doctor slots, and bed availability with an admin analytics dashboard.
# 🏥 NHM Hospital Resource Monitoring System

## 📋 Overview

The **NHM (National Health Mission) Hospital Resource Monitoring System** is a comprehensive real-time healthcare management platform designed to streamline hospital operations, bed tracking, appointment scheduling, and resource allocation across multiple healthcare facilities.

## ✨ Features

### 🔐 Multi-Role Authentication
- **Patients**: Book appointments, view bed availability, access medical reports
- **Hospital Admins**: Manage wards, doctors, appointments, and bed occupancy
- **NHM Officials**: Centralized monitoring across all hospitals

### 🏥 Hospital Management
- **Real-time Bed Tracking**: Monitor occupancy across General, ICU, Emergency, and Maternity wards
- **Doctor Management**: Track doctor availability, specializations, and schedules
- **Appointment System**: Book, cancel, and manage patient appointments
- **Emergency Mode**: Activate disaster protocols with priority resource allocation

### 📊 Analytics Dashboard
- Live statistics on bed occupancy
- Doctor availability tracking
- Appointment trends
- Hospital-wise resource distribution

### 💊 Additional Modules
- **Digital Pharmacy**: Medicine ordering with Razorpay integration
- **Blood Bank Management**: Real-time blood inventory tracking
- **Lab Tests**: Home sample collection booking
- **Medical Report Analyzer**: AI-powered report summarization
- **Government Policies**: NHM scheme information and eligibility checker

### 🏢 Multi-Hospital Support
- Switch between multiple hospitals
- Centralized NHM admin view
- Dynamic hospital registration

## 🛠️ Technology Stack

### Frontend
- **HTML5**: Structure and semantics
- **CSS3**: Custom styling with CSS variables
- **JavaScript (ES6+)**: Dynamic functionality
- **Font Awesome 6**: Icons and visual elements
- **Google Fonts (Inter)**: Typography

### Backend
- **Node.js**: Server runtime
- **Express.js**: API framework
- **File System (fs)**: JSON-based data storage

### Payment Integration
- **Razorpay**: Secure payment processing for pharmacy orders

## 📁 Project Structure

```
NHM-Hospital-Monitor/
├── 📄 index.html              # Patient login portal
├── 📄 head.html                # Landing page
├── 📄 login.html               # Role selection
├── 📄 hospital_login.html      # Hospital admin login
├── 📄 nhm_login.html           # NHM official login
├── 📄 hospital_dashboard.html   # Hospital admin dashboard
├── 📄 admin_dashboard.html      # NHM central dashboard
├── 📄 about.html               # About page
├── 📄 contact.html             # Contact form
├── 📄 blood-bank.html          # Blood bank module
├── 📄 pharmacy.html            # Digital pharmacy
├── 📄 lab-tests.html           # Lab test booking
├── 📄 reports.html             # Medical report analyzer
├── 📄 policies.html            # Government policies
├── 📄 hosp1-6.html             # Individual hospital dashboards
│
├── 📄 app.js                   # Main application logic
├── 📄 head.js                   # Landing page scripts
├── 📄 pharmacy.js               # Pharmacy module logic
├── 📄 hosp1-6.js                # Individual hospital logic
│
├── 📄 styles.css                # Global styles
├── 📄 head.css                   # Landing page styles
├── 📄 style.css                  # Contact form styles
│
├── 📄 server.js                  # Node.js backend
├── 📄 package.json               # Dependencies
├── 📄 db.json                    # Main database
├── 📄 credentials.json           # Hospital credentials
├── 📄 contacts.json              # Contact form submissions
│
└── 📄 README.md                  # Documentation
```

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- npm (Node Package Manager)
- Modern web browser

### Step-by-Step Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/nhm-hospital-monitor.git
cd nhm-hospital-monitor
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure Razorpay (Optional)**
- Open `pharmacy.js`
- Replace `YOUR_RAZORPAY_KEY_ID` with your actual Razorpay key

4. **Start the server**
```bash
npm start
# or
node server.js
```

5. **Access the application**
- Open browser and navigate to: `http://localhost:3000`
- Or open any HTML file directly (for static mode)

## 🔑 Login Credentials

### Demo Accounts

#### Patient Access
- Any ID works (e.g., `patient123`)
- Password: any value

#### Hospital Admin
| Hospital ID | Password | Hospital Name |
|------------|----------|---------------|
| HOSP-MUM-01 | admin123 | Tata Memorial Centre |
| HOSP-MUM-02 | admin123 | Kokilaben Hospital |
| HOSP-MUM-03 | admin123 | Lilavati Hospital |
| HOSP-MUM-04 | admin123 | Jaslok Hospital |
| HOSP-MUM-05 | admin123 | HN Reliance Hospital |
| HOSP-MUM-06 | admin123 | Fortis Hospital |

#### NHM Official
- ID: `nhm-admin` or `admin`
- Password: `NHM-ADMIN`

## 💡 Usage Guide

### For Patients
1. Visit `index.html`
2. Login with any ID
3. Select your city and hospital
4. Book appointments, check bed availability
5. Access pharmacy, lab tests, and medical reports

### For Hospital Admins
1. Visit `hospital_login.html`
2. Enter Hospital ID and password
3. Manage wards (admit/discharge patients)
4. Track doctor availability
5. View and manage appointments
6. Activate emergency mode if needed

### For NHM Officials
1. Visit `nhm_login.html`
2. Use NHM credentials
3. Monitor all hospitals from central dashboard
4. Switch between hospitals using hospital switcher
5. View system-wide statistics and logs

## 🔧 Key Functionalities

### Bed Management
- Real-time occupancy tracking
- Visual bed grid with tooltips
- Filter by ward type (ICU, General, Emergency, Maternity)
- Admit/Discharge patients

### Appointment System
- Department-based doctor selection
- Real-time slot availability
- Email confirmation simulation
- Appointment cancellation

### Hospital Switcher
- Toggle between all hospitals
- View aggregated statistics
- Filter beds by hospital
- Compare resource allocation

### Emergency Mode
- One-click activation
- Reserves beds for emergencies
- Alerts all staff
- Pauses routine bookings

## 🌐 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/register` | POST | Register new user |
| `/api/login` | POST | User authentication |
| `/api/wards` | GET | Fetch ward data |
| `/api/wards/update` | POST | Update ward occupancy |
| `/api/medicine-orders` | POST | Save medicine orders |
| `/api/medicine-orders/:userId` | GET | Get user order history |
| `/api/contacts` | GET/POST | Contact form submissions |

## 🎨 UI/UX Highlights

- **Responsive Design**: Works on desktop, tablet, and mobile
- **Real-time Updates**: Live data refresh every 2 seconds
- **Toast Notifications**: User feedback for actions
- **Dark/Light Mode**: Adaptive color schemes
- **Accessibility**: ARIA labels and keyboard navigation
- **Animations**: Smooth transitions and hover effects

## 🔒 Security Features

- Role-based access control
- Session management with localStorage
- Secure password handling
- CORS configuration for API
- Input validation and sanitization

## 🧪 Testing

Run the application and test:
1. User authentication flows
2. Bed occupancy updates
3. Appointment booking
4. Hospital switching
5. Emergency mode activation
6. Pharmacy checkout
7. Contact form submissions

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is created for educational and demonstration purposes as part of a hackathon submission.

## 👥 Team

- Project Lead: [Your Name]
- Frontend Developer: [Team Member]
- Backend Developer: [Team Member]
- UI/UX Designer: [Team Member]

## 🙏 Acknowledgments

- National Health Mission (NHM) for inspiration
- Font Awesome for icons
- Google Fonts for typography
- Razorpay for payment integration
- Unsplash for stock images

## 📧 Contact

For support or queries:
- Email: support@nhmportal.gov.in
- Helpline: +91-1800-419-4444

---

**Built with ❤️ for the NHM Hackathon 2026**
