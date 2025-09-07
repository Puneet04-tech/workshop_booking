# **Workshop Booking System - UI/UX Enhancement**

> **FOSSEE Python Screening Task 1** - Enhanced UI/UX for mobile-first workshop booking platform

This website is for coordinators to book workshops. They can book workshops based on instructor posts or propose workshop dates based on their convenience.

## Before Enhancement
![Before Screenshot - Original Design](docs/screenshots/before-homepage.png)
![Before Screenshot - Workshop Details](docs/screenshots/before-workshop-details.png)

## After Enhancement  
![After Screenshot - Enhanced Homepage](docs/screenshots/after-homepage.png)
![After Screenshot - Enhanced Workshop Details](docs/screenshots/after-workshop-details.png)

## Design Principles & Reasoning

### 1. What design principles guided your improvements?

**Mobile-First Approach**: Started with mobile layout and enhanced for larger screens
- Used CSS Grid and Flexbox for responsive layouts
- Implemented touch-friendly button sizes (minimum 44px)
- Optimized typography scale for readability on small screens

**Visual Hierarchy**: Clear information architecture
- Used consistent spacing scale (8px base unit)
- Implemented proper heading hierarchy (H1-H6)
- Applied color coding for status indicators
- Enhanced contrast ratios for accessibility (WCAG AA compliant)

**Modern Card-Based Layout**: Replaced basic tables with card components
- Improved scanability of workshop information
- Better visual grouping of related data
- Enhanced mobile interaction patterns

### 2. How did you ensure responsiveness across devices?

**CSS Grid & Flexbox**: Fluid layouts that adapt to screen size
- Responsive navigation with mobile hamburger menu
- Flexible card layouts that reflow on smaller screens
- Optimized form layouts for mobile input

**Breakpoint Strategy**:
- Mobile: 320px - 768px (primary focus)
- Tablet: 768px - 1024px
- Desktop: 1024px+

**Performance Considerations**:
- Optimized images with responsive sizing
- Minimal CSS animations for smooth mobile performance
- Efficient CSS selectors

### 3. What trade-offs did you make between design and performance?

**CSS Framework**: Kept Bootstrap but added custom CSS for enhancements
- **Trade-off**: Slightly larger CSS bundle vs faster development
- **Decision**: Optimized by using only required Bootstrap components

**Icon Usage**: Used Material Icons CDN vs custom icons
- **Trade-off**: External dependency vs file size
- **Decision**: CDN for faster loading and consistent iconography

**Image Optimization**: Used CSS gradients instead of background images where possible
- **Trade-off**: Some visual fidelity vs faster loading
- **Decision**: Prioritized performance for mobile users

### 4. What was the most challenging part of the task and how did you approach it?

**Challenge**: Maintaining Django template structure while modernizing UI
- **Approach**: Enhanced existing templates without breaking functionality
- **Solution**: Added progressive enhancement with CSS and minimal JavaScript

**Challenge**: Mobile navigation with complex menu structure
- **Approach**: Implemented collapsible navigation with improved touch targets
- **Solution**: Used Bootstrap's responsive utilities with custom enhancements

## Technical Implementation

### Changes Made:
- [x] Mobile-first responsive design
- [x] Enhanced navigation with improved mobile experience
- [x] Card-based layout for better visual hierarchy
- [x] Improved color scheme and typography
- [x] Better accessibility features (ARIA labels, contrast)
- [x] Performance optimizations
- [x] Modern CSS Grid and Flexbox layouts
- [x] Touch-friendly interface elements

### New Features:
- Responsive workshop cards with status indicators
- Improved comment system with better visual hierarchy
- Enhanced form layouts for mobile
- Loading states and micro-interactions
- Better error and success messaging

### Features
* Statistics
    1. Instructors Only
        * Monthly Workshop Count
        * Instructor/Coordinator Profile stats
        * Upcoming Workshops
        * View/Post comments on Coordinator's Profile
    2. Open to All
        * Workshops taken over Map of India
        * Pie chart based on Total Workshops taken to Type of Workshops.

* Workshop Related Features
    > Instructors can Accept, Reject or Delete workshops based on their preference, also they can postpone a workshop based on coordinators request.

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/FOSSEE/workshop_booking.git
   cd workshop_booking
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Setup database**
   ```bash
   python manage.py makemigrations
   python manage.py makemigrations cms
   python manage.py migrate
   ```

5. **Create superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Run development server**
   ```bash
   python manage.py runserver
   ```

7. **Access application**
   - Open browser and navigate to: http://127.0.0.1:8000/

## Technology Stack

- **Backend**: Django 3.0.7
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Bootstrap 4 (Enhanced)
- **Icons**: Material Icons
- **Database**: SQLite (Development)
- **Charts**: Chart.js

## Browser Support

- Chrome 70+
- Firefox 65+
- Safari 12+
- Edge 79+
- Mobile Safari iOS 12+
- Chrome Mobile 70+

## Performance Metrics

- **Mobile PageSpeed**: 90+ (Target)
- **Desktop PageSpeed**: 95+ (Target)
- **First Contentful Paint**: <2s
- **Largest Contentful Paint**: <3s

__NOTE__: Check docs/Getting_Started.md for more info.
