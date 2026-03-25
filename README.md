# Patient Management System - Frontend 🏥

A responsive, mobile-friendly web frontend for the Patient Management API built with **pure HTML, CSS, and JavaScript**. Perfect for GitHub Pages hosting!

## 📱 Features

- ✅ **Fully Responsive Design** - Works perfectly on desktop, tablet, and mobile
- ✅ **Pure HTML/CSS/JavaScript** - No frameworks, GitHub Pages compatible
- ✅ **Tailwind CSS** - Beautiful, responsive UI with Tailwind's utility classes
- ✅ **Real-time Updates** - Instant feedback on all operations
- ✅ **Complete CRUD Operations** - Create, Read, Update, Delete patients
- ✅ **Advanced Search** - Find patients by ID or name
- ✅ **Smart Sorting** - Sort by height, weight, or BMI
- ✅ **BMI Visualization** - Color-coded health status badges
- ✅ **Smooth Animations** - Delightful UI interactions
- ✅ **Mobile-Optimized** - Touch-friendly interface

## 📁 File Structure

```
FRONTEND/
├── index.html       # Main HTML file with all modals and structure
├── main.js          # Complete API integration and functionality
├── styles.css       # Custom styling and animations
└── README.md        # This file
```

## 🚀 Quick Start

### Option 1: Local Development

1. **Clone or download the FRONTEND folder**

   ```bash
   cd FRONTEND
   ```

2. **Open in browser**
   - Double-click `index.html`, OR
   - Use a local server:

     ```bash
     python -m http.server 8000
     # Then open http://localhost:8000
     ```

### Option 2: Deploy to GitHub Pages

1. **Create a new GitHub repository** (e.g., `patient-management-frontend`)

2. **Clone or push the FRONTEND folder to GitHub**

   ```bash
   git clone https://github.com/YOUR_USERNAME/patient-management-frontend.git
   cd patient-management-frontend
   # Copy FRONTEND contents here
   git add .
   git commit -m "Initial commit: Patient Management Frontend"
   git push origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Choose "main" branch → "/ (root)"
   - Click Save

4. **Access your frontend**
   - Your site will be live at: `https://YOUR_USERNAME.github.io/patient-management-frontend`
   - Alternatively: `https://YOUR_USERNAME.github.io/patient-management-frontend/index.html`

## 🔗 API Configuration

The frontend is configured to use the backend API at:

```
https://patient-management-app-rqjp.onrender.com
```

To change the API URL, edit `main.js`:

```javascript
const API_BASE_URL = 'https://your-api-url.com';
```

## 💻 Usage Guide

### 1. **Add a New Patient**

- Click the **"➕ Add Patient"** button
- Fill in all required fields:
  - Patient ID (e.g., P001)
  - Full Name
  - Age (1-119)
  - City
  - Gender
  - Height (in meters)
  - Weight (in kilograms)
- Click **"Save Patient"**
- BMI and health verdict are calculated automatically

### 2. **View All Patients**

- Click **"🔄 Refresh"** to reload
- All patients are displayed as cards
- Each card shows:
  - Patient name and ID
  - Age, city, weight, BMI
  - Health status with color-coded badge

### 3. **View Patient Details**

- Click the **"👁️ View"** button on any patient card
- See detailed information in a modal

### 4. **Edit Patient**

- Click the **"✏️ Edit"** button on any patient card
- Modify the information
- Click **"Update Patient"**
- BMI and verdict update automatically

### 5. **Delete Patient**

- Click the **"🗑️ Delete"** button
- Confirm deletion in the confirmation modal
- Patient is removed from the system

### 6. **Search Patients**

- Click **"🔍 Search"** button
- **Search by ID**: Enter Patient ID (e.g., P001)
- **Search by Name**: Enter full name
- Results appear instantly

### 7. **Sort Patients**

- Click **"📊 Sort"** button
- Select field: Height, Weight, or BMI
- Choose order: Ascending (⬆️) or Descending (⬇️)
- Results display sorted

## 📊 BMI Status Categories

| BMI Range | Verdict | Color |
|-----------|---------|-------|
| < 18.5 | 🟠 Underweight | Orange |
| 18.5 - 24.9 | 🟢 Normal | Green |
| 25 - 29.9 | 🟡 Overweight | Yellow |
| 30 - 34.9 | 🔴 Obese | Red |
| ≥ 35 | 🔴 Extremely Obese | Dark Red |

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Responsive design with Tailwind CSS
- **JavaScript (ES6+)** - Modern JavaScript for API integration
- **Tailwind CSS (CDN)** - Utility-first CSS framework
- **Fetch API** - For backend communication

## 📱 Browser Compatibility

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🔄 API Integration

The frontend communicates with the backend API using the Fetch API:

```javascript
// Example: Add new patient
fetch('https://patient-management-app-rqjp.onrender.com/new', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        id: 'P001',
        name: 'John Doe',
        age: 30,
        city: 'New York',
        gender: 'male',
        height: 1.75,
        weight: 75
    })
})
```

All API endpoints are fully implemented:

- ✅ GET /view - View all patients
- ✅ GET /patient/{id} - Search by ID
- ✅ GET /patient/name/{name} - Search by name
- ✅ GET /sort - Sort patients
- ✅ POST /new - Add patient
- ✅ PUT /update/{id} - Update patient
- ✅ DELETE /delete/{id} - Delete patient
