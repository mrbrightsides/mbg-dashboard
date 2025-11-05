# MBG Dashboard 🍱

**Makan Bergizi Gratis - Smart Distribution & Monitoring System**

A comprehensive web application designed to transform the distribution and monitoring of Indonesia's Free Nutritious Meals (Makan Bergizi Gratis) program. This platform ensures transparency, efficiency, and accountability in getting meals from kitchens to students across the nation.

[![Built with Next.js](https://img.shields.io/badge/Next.js-14-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)](https://www.typescriptlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

## 🌟 Overview

The MBG Dashboard addresses critical challenges in Indonesia's school meal distribution:
- **Distribution chaos** → Real-time tracking and coordination
- **Lack of monitoring** → Live dashboards with full visibility
- **Supply chain opacity** → End-to-end transparency with blockchain
- **Manual processes** → Automated workflows and AI optimization

---

## 🚀 Key Features

### 📊 Multi-Role System
- **Admin Dashboard**: Full oversight, analytics, and system management
- **Driver Dashboard**: Route optimization, delivery tracking, and mobile tools
- **School Dashboard**: Meal tracking, QR verification, and scheduling

### 🗺️ Real-Time Tracking
- Live delivery maps with GPS tracking
- Geofencing alerts when drivers enter school zones
- Route visualization and optimization
- Status updates across all stakeholders

### ⛓️ Blockchain Transparency
- Immutable delivery records
- Complete audit trails
- Hash verification for data integrity
- Government compliance ready

### 🤖 AI-Powered Features
- **Route Optimization**: Reduce fuel costs and delivery time
- **Demand Forecasting**: Predict meal requirements 7 days ahead
- **AI Chatbot**: Intelligent Q&A assistant
- **Voice Commands**: Hands-free operation for drivers

### 📱 Mobile-First Design
- Progressive Web App (PWA) support
- Offline capability
- Touch-optimized controls
- Installable on any device

### 💬 Multi-Channel Notifications
- Push notifications
- WhatsApp integration
- In-app messaging
- Email alerts (coming soon)

### 📸 Verification Systems
- QR code generation and scanning
- Photo verification of deliveries
- Digital signatures
- Timestamp tracking

### 🌍 Accessibility
- Bilingual support (Bahasa Indonesia & English)
- Weather monitoring and alerts
- Responsive design for all screen sizes
- WCAG accessibility standards

---

## 🛠️ Technology Stack

### Frontend
- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS
- **UI Components**: shadcn/ui, Radix UI
- **State Management**: React Context API

### Maps & Location
- **react-leaflet**: Interactive maps
- **Geolocation API**: GPS tracking
- **Geofencing**: Zone-based alerts

### Data Visualization
- **Recharts**: Charts and analytics
- **React**: Real-time data updates

### QR & Scanning
- **qrcode.react**: QR code generation
- **html5-qrcode**: Camera scanning

### PWA & Offline
- **Service Workers**: Offline support
- **Web App Manifest**: Installation
- **IndexedDB**: Local storage

### Voice & AI
- **Web Speech API**: Voice recognition
- **Speech Synthesis**: Text-to-speech
- **Custom AI**: Chatbot logic

---

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- npm or yarn

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/mrbrightsides/mbg-dashboard.git
   cd mbg-dashboard
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run development server**
   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:3000
   ```

---

## 🎯 Usage

### Quick Login (Demo Mode)

The application includes quick login buttons for testing:

- **Admin** → Full system access
- **Driver (Agus)** → Delivery management view
- **School (SDN 01)** → Meal tracking view

### Manual Login

Enter credentials:
- **Username**: admin / driver / school
- **Password**: Any password (demo mode)

---

## 📱 Features by Role

### 🏛️ Admin Dashboard (14 Tabs)
1. **Overview** - KPIs, delivery statistics
2. **Live Map** - Real-time GPS tracking
3. **Analytics** - Charts and insights
4. **History** - Searchable records with CSV export
5. **Notifications** - Push notification management
6. **Route AI** - AI-powered route optimization
7. **Performance** - Driver leaderboard and metrics
8. **Predictions** - 7-day demand forecasting
9. **Weather** - Regional weather monitoring
10. **AI Chat** - Intelligent chatbot assistant
11. **Voice** - Voice command interface
12. **Blockchain** - Immutable ledger explorer
13. **WhatsApp** - Message broadcasting system
14. **Geofencing** - Zone monitoring and alerts

### 🚚 Driver Dashboard (6 Tabs)
1. **My Deliveries** - Assigned routes and tasks
2. **Route Map** - Visual route planning
3. **Photo Verification** - Camera capture for proof
4. **Notifications** - Real-time updates
5. **Weather** - Current conditions for route
6. **Voice** - Hands-free controls while driving

### 🏫 School Dashboard (2 Tabs)
1. **Delivery Schedule** - Incoming meal tracker
2. **Verify Delivery** - QR code scanner

---

## 🌐 API Integration

### Proxy Endpoint

All external API calls use the proxy endpoint at `/api/proxy`:

```typescript
const response = await fetch('/api/proxy', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    protocol: 'https',
    origin: 'api.example.com',
    path: '/endpoint',
    method: 'GET',
    headers: {},
    // body: {} // optional
  }),
});
```

---

## 🏗️ Project Structure

```
mbg-dashboard/
├── src/
│   ├── app/
│   │   ├── about/          # About page
│   │   ├── admin/          # Admin dashboard
│   │   ├── driver/         # Driver dashboard
│   │   ├── school/         # School dashboard
│   │   ├── api/            # API routes
│   │   ├── layout.tsx      # Root layout
│   │   └── page.tsx        # Login page
│   ├── components/
│   │   ├── ui/             # shadcn/ui components
│   │   ├── AdminDashboard.tsx
│   │   ├── DriverDashboard.tsx
│   │   ├── SchoolDashboard.tsx
│   │   ├── DashboardLayout.tsx
│   │   ├── Footer.tsx
│   │   └── [feature-components]/
│   ├── contexts/
│   │   ├── AuthContext.tsx
│   │   ├── LanguageContext.tsx
│   │   └── DeliveryContext.tsx
│   └── lib/
│       └── utils.ts
├── public/
│   ├── manifest.json       # PWA manifest
│   └── service-worker.js   # Service worker
├── README.md
├── package.json
└── tsconfig.json
```

---

## 🎨 Design System

### Color Palette
- **Primary**: Green 600 → Emerald 600 (MBG brand)
- **Accents**: Blue, Purple, Pink, Cyan
- **Status Colors**:
  - 🟢 Green: Delivered / Success
  - 🟡 Yellow: In Transit / Warning
  - 🔴 Red: Failed / Error
  - 🔵 Blue: Pending / Info

### Typography
- **Headings**: Bold, gradient text effects
- **Body**: Clear hierarchy with proper contrast
- **Accessibility**: WCAG AA compliant

---

## 📊 Data Model

### Core Entities

```typescript
interface User {
  id: string;
  name: string;
  role: 'admin' | 'driver' | 'school';
  region: string;
}

interface Delivery {
  id: string;
  schoolId: string;
  driverId: string;
  status: 'pending' | 'in_transit' | 'delivered' | 'failed';
  mealCount: number;
  scheduledTime: string;
  actualTime?: string;
  location?: { lat: number; lng: number };
}

interface School {
  id: string;
  name: string;
  address: string;
  region: string;
  studentCount: number;
  location: { lat: number; lng: number };
}
```

---

## 🔐 Security

- Role-based access control (RBAC)
- Client-side authentication (demo mode)
- Blockchain verification for data integrity
- Secure API proxy for external calls
- Input validation and sanitization

---

## 🌍 Internationalization

Supported languages:
- 🇮🇩 Bahasa Indonesia
- 🇬🇧 English

250+ translated strings across the entire application.

---

## 📈 Performance

- **Bundle Size**: ~460 KB (optimized)
- **Build Time**: ~45 seconds
- **Lighthouse Score**: 90+ (target)
- **Mobile Performance**: Optimized with lazy loading

---

## 🚀 Deployment

### Vercel (Recommended)

1. Push code to GitHub
2. Import project in Vercel
3. Deploy automatically

### Docker

```bash
docker build -t mbg-dashboard .
docker run -p 3000:3000 mbg-dashboard
```

### Manual

```bash
npm run build
npm start
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Indonesian Government** for the MBG program initiative
- **Schools and drivers** who inspired this solution
- **Open source community** for amazing tools and libraries

---

## 📞 Contact & Credits

**Built with 💚 by**

- **GitHub**: [@mrbrightsides](https://github.com/mrbrightsides)
- **Website**: [rantai.elpeef.com](https://rantai.elpeef.com)

---

## 🎯 Roadmap

### Phase 5 (Future)
- [ ] Telegram integration
- [ ] SMS fallback notifications
- [ ] Biometric verification
- [ ] AI computer vision for food quality
- [ ] Parent portal
- [ ] Nutrition tracking per student
- [ ] Waste management tracking
- [ ] Integration with government systems

---

## 💡 Impact

This platform aims to:
- ✅ Ensure **100% transparency** in meal distribution
- ✅ Serve **50,000+ students** across Indonesia
- ✅ Reduce **waste and delays** through optimization
- ✅ Provide **accountability** via blockchain
- ✅ Empower **government and NGOs** with data-driven decisions

---

**Made with ❤️ for Indonesia's children** 🇮🇩
