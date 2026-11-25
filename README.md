# THEATRON CINEMA LOUNGES — MEMBER 4 FRONTEND SUITE
### User Profile • Offers • Cinemas

> **Premium Luxury Cinematic Website | Production-Quality Frontend | Fully Responsive**  
> **Built exclusively with HTML5, CSS3, and Vanilla JavaScript (ES6+)**  
> **Strictly zero frameworks, zero external dependencies.**

---

## 1. Executive Summary

This project delivers the complete, production-grade frontend implementation for **Member 4** of the **THEATRON CINEMA LOUNGES** booking platform.

Following the exact visual identity, luxury cinema atmosphere, and typography of the reference website screenshots, this implementation features:
- **Brand Palette:** Deep Burgundy (`#3A0D18`), Deep Maroon (`#4B101E`), Midnight Obsidian Black (`#090607`, `#12090C`), Metallic Champagne Gold (`#E6B96F`), and Gold Highlight (`#F1BD72`).
- **Typography:** High-end editorial serif (`Cinzel` & `Playfair Display`) paired with clean modern sans-serif (`Montserrat`).
- **Signature UI Elements:** Gold-bordered square **T** logo, "CINEMA LOUNGES" tracked subtitle, gold hairline card borders, dark glassmorphic surfaces, tickets counter button with circular badge (`6`), and responsive mobile drawer navigation.

---

## 2. Project File Structure

```
THEATRON-MEMBER-4/
│
├── index.html              # Member 4 Master Overview Portal & Gateway
├── profile.html            # Page 1: Luxury User Profile & Connoisseur Dashboard
├── offers.html             # Page 2: Exclusive Privileges & Promo Catalogue
├── cinemas.html            # Page 3: Signature Cinema Destinations Directory
│
├── css/
│   ├── style.css           # Global design tokens, typography, shared header, drawer & footer
│   ├── profile.css         # User profile hero, 3D card, animated stats, forms & activity
│   ├── offers.css          # Offers hero, featured truffle banner, filter tabs, catalogue & FAQ
│   ├── cinemas.css         # Cinemas hero, live search bar, cards, interactive map & tech showcase
│   ├── animations.css      # Canvas particles, 3D tilt, gold shimmer, scroll reveal & transitions
│   └── responsive.css      # Strict responsive media queries (360px up to 4K displays)
│
├── js/
│   ├── main.js             # Sticky header, mobile navigation drawer, tickets modal & toast engine
│   ├── animations.js       # Canvas gold dust particles, IntersectionObserver, 3D tilt & counters
│   ├── profile.js          # Profile state management, form validation, LocalStorage & pass modal
│   ├── offers.js           # Instant category filter, Clipboard API promo copy & offer modal
│   └── cinemas.js          # Live search & filtering, sorting, interactive map pins & cinema modal
│
├── assets/
│   ├── images/             # Vector cinema renders, posters, avatar & offer visuals
│   │   ├── luxury-avatar.svg
│   │   ├── flagship-cinema.svg
│   │   ├── elysium-palace.svg
│   │   ├── celestial-pavilion.svg
│   │   ├── astral-sanctuary.svg
│   │   ├── doomsday-poster.svg
│   │   ├── mirage-poster.svg
│   │   ├── symphony-poster.svg
│   │   ├── offer-truffle.svg
│   │   ├── offer-weekday.svg
│   │   ├── offer-duo.svg
│   │   ├── offer-lounge.svg
│   │   ├── offer-premiere.svg
│   │   └── offer-snack.svg
│   ├── icons/              # Embedded SVG icons & system glyphs
│   └── logos/
│       └── theatron-logo.svg # Official THEATRON gold-bordered square T mark
│
└── README.md               # Technical documentation & testing report
```

---

## 3. Detailed Page Implementations

### Page 1: User Profile (`profile.html`)
- **Profile Hero Section:** Connoisseur greeting, user avatar with gold border and live status indicator, full name ("Lord Alistair Vance"), email, membership ID (`TH-9842-ROYAL`), membership level badge (`ROYAL GOLD CONNOISSEUR`), member since date, and interactive "Edit Profile" button.
- **3D Digital Membership Card:** Interactive perspective tilt on mouse movement and touch, metallic sheen gradient, gold chip, stylized QR code, and click-to-copy card number.
- **Animated Statistics:** Four statistics cards featuring dynamic `requestAnimationFrame` animated counters:
  - Total Movies Watched: **42**
  - Total Tickets Booked: **68**
  - Loyalty Points: **14,850 PTS**
  - Total Luxury Concessions: **$3,420**
- **Personal Information (Editable):** Form with Full Name, Email Address, Telephone, Date of Birth, Gender, Language, and Residence. Includes client-side validation (regex email validation, required checks), "Save Changes" and "Cancel" states, and **LocalStorage persistence** so updates survive page reloads.
- **My Preferences:** Dropdown selector for Home Sanctuary, selectable interactive genre chips (*Sci-Fi Thriller, Mystery, Historical Drama*), and three custom animated toggle switches for Email, Promotional, and Showtime notifications (persisted to LocalStorage).
- **Membership Benefits:** Four cards detailing Gala Priority Booking, Artisan Velvet Lounge Access, In-Seat Butler Dining, and Complimentary Valet Parking.
- **Recent Activity:** Showtime archive showcasing realistic booking demonstration data (*DOOMSDAY: ECLIPSE PROTOCOL, MIRAGE OF KINGS, SYMPHONY FOR ZERO*) with status badges and an interactive "View Digital Pass" modal with QR code.

### Page 2: Offers & Privileges (`offers.html`)
- **Offers Hero:** Cinematic hero banner with champagne gold animated typography, "THEATRON PRIVILEGE SUITE" badge, and dark maroon atmospheric background.
- **Featured Privilege Banner:** Prominent banner inspired directly by the reference screenshot:
  - *PRIVATE LOUNGE PRIVILEGE — COMPLIMENTARY TRUFFLE SERVICE WITH CODE GOLD15*
  - "Book With Privilege" gold gradient button and "Explore Benefits" outline button.
- **Category Filter Tabs:** Instant client-side filtering without page reloads across **All Offers**, **Exclusive**, **Food & Beverages**, **Membership**, **Ticket Discounts**, and **Special Events**.
- **Demonstration Offers Catalogue:**
  1. `GOLD15`: 15% off Royal Gold Recliner tickets with truffle service.
  2. `WEEKDAY20`: 20% off selected weekday screenings.
  3. `DUO25`: 25% discount on couple/two-person velvet suite bookings.
  4. `LOUNGEVIP`: Exclusive velvet lounge access & sommelier greeting.
  5. `PREMIERE10`: 10% discount on red carpet gala previews.
  6. `SNACKCOMBO`: 30% savings on organic truffle popcorn & craft mocktails.
- **Promo Code Clipboard System:** "Copy Code" button copies code directly via the modern `navigator.clipboard` API (with fallback), changes button label to **Copied!**, and triggers a gold luxury toast notification.
- **Offer Details Modal:** Opens full modal with title, discount breakdown, validity dates, terms, and simulated "Apply Privilege Now" workflow.
- **How to Redeem & FAQ:** Step-by-step numbered guide and collapsible FAQ accordion.

### Page 3: Signature Cinemas (`cinemas.html`)
- **Cinemas Hero:** "SIGNATURE CINEMAS — Discover Extraordinary Cinema Destinations" with floating gold particle ambiance.
- **Search & Multi-Facet Filters:**
  - Real-time text search by cinema name or address.
  - Dropdown filter by city/metropolis.
  - Interactive facility chips filter: *Dual-Laser IMAX, Dolby Atmos, Royal Gold Lounge, In-Seat Butler Dining, ScreenX 270°, 70mm Film*.
  - Sort dropdown: *Halls (High to Low / Low to High)* and *Name (A—Z)*.
  - "Reset Filters" action.
- **Signature Cinema Cards:**
  - **THEATRON GRAND FLAGSHIP** (88 Sovereign Boulevard, Suite 100 — 8 Halls, Dual-Laser IMAX, Dolby Atmos, Royal Gold Lounge, Luxury Concessions, Valet).
  - **THEATRON ELYSIUM PALACE** (420 Monarch Avenue, Royal Heights — 6 Halls, Dolby Cinema, Sovereign Velvet Suites, Sommelier Cellar).
  - **THEATRON CELESTIAL PAVILION** (15 Aurora Crest Drive, Skyline Plaza — 10 Halls, 70mm Projector, Dual-Laser IMAX, Mezzanine Lounge).
  - **THEATRON ASTRAL SANCTUARY** (77 Marina Promenade, Pier 4 — 5 Halls, ScreenX 270°, Dolby Atmos, Waterfront Terrace).
- **Interactive Visual Map Explorer:** Stylized dark coordinate grid with clickable golden hotspot pins that highlight destinations and update the location summary pane in real time.
- **Cinema Details Modal:** Rich modal displaying architectural renders, hall count, acoustic audio engines, seating configurations, dining menu, and operating hours.
- **Cinema Experience Section:** Feature cards detailing Dual-Laser IMAX 4K, Royal Gold Recliners, Dolby Atmos Soundscape, Acoustic Maroon Velvet Lounges, and Artisan Concessions.

---

## 4. Animation Engine

All animations are crafted using pure CSS3 and Vanilla JavaScript:
1. **Ambient Gold Dust Particles:** Dynamic HTML5 Canvas particle generator with gentle floating drift, wrapping boundaries, and pulsation.
2. **Scroll Reveal:** Smooth entrance animations powered by `IntersectionObserver`.
3. **3D Card Perspective Tilt:** Interactive mouse-tracking tilt effect with dynamic radial glare lighting (`.tilt-card`).
4. **Animated Counters:** Smooth cubic-eased numerical incrementing (`requestAnimationFrame`).
5. **Toast Notification System:** Slide-up gold notifications for copy operations, preference changes, and booking confirmations.
6. **Accessibility (`prefers-reduced-motion`):** Automatically disables heavy animations and canvas processing for users requesting reduced motion.

---

## 5. Instructions for Running Locally

The project runs directly in any modern web browser without needing a compilation step or web server:

### Option A: Direct File Open
1. Unzip `THEATRON-MEMBER-4.zip`.
2. Double-click `index.html` to open the Member 4 Overview Portal in your web browser (Chrome, Edge, Safari, Firefox).
3. Navigate seamlessly between **User Profile**, **Offers**, and **Cinemas** using the header navigation.

### Option B: Local Web Server (Optional)
If you prefer running via a local HTTP server:
```bash
# Using Python:
cd THEATRON-MEMBER-4
python -m http.server 8000

# Open in browser:
http://localhost:8000/
```

---

## 6. Testing & Quality Assurance Report

The entire suite was tested across desktop and mobile viewports:

| Test Item | Tested Scenario | Result |
| :--- | :--- | :--- |
| **Cross-Page Navigation** | Navigation between `index.html`, `profile.html`, `offers.html`, `cinemas.html` | ✅ Passed. All links and active states accurate. |
| **Mobile Drawer** | Hamburger click, outside backdrop tap, Escape key press | ✅ Passed. Smooth sliding drawer and backdrop blur. |
| **Tickets Counter Modal** | Click on "Tickets (6)" in header | ✅ Passed. Displays reserved Doomsday screening details. |
| **Profile Editing** | Edit form, modify fields, validation check, click Cancel | ✅ Passed. Reverts correctly to initial state. |
| **Profile Persistence** | Edit name/email, click Save Changes, refresh browser | ✅ Passed. LocalStorage successfully restores modified values. |
| **Preferences Switches** | Toggle notification switches and genre chips, refresh | ✅ Passed. Settings immediately saved and restored. |
| **Offers Filter Tabs** | Switch between All, Exclusive, Food, Membership, Tickets | ✅ Passed. Cards filter smoothly with transition. |
| **Promo Code Copy** | Click "Copy Code" on cards and modal | ✅ Passed. Copies to clipboard, button displays "Copied!", gold toast alert fires. |
| **Offer Details Modal** | Click "View Details" or "Redeem Now" | ✅ Passed. Modal populates correct code and terms. |
| **Cinema Live Search** | Type "Flagship", "Elysium", "Boulevard", "Marina" | ✅ Passed. Cards filter in real time. |
| **Cinema Facility Filters**| Toggle "Dual-Laser IMAX", "Dolby Atmos", "ScreenX" | ✅ Passed. Accurately matches facility tags. |
| **Interactive Map Pins** | Click pins on metropolitan map grid | ✅ Passed. Updates summary pane and highlights target cinema card. |
| **Cinema Details Modal** | Click "View Details" on cinema card | ✅ Passed. Displays complete architectural and audio specifications. |
| **Mobile Viewport 360px** | Small Android screen test | ✅ Passed. No horizontal overflow, readable fonts, touch-friendly buttons. |
| **Mobile Viewport 390px** | iPhone 14/15/16 screen test | ✅ Passed. Single-column card stacking, comfortable touch targets. |
| **Tablet Viewport 768px** | iPad screen test | ✅ Passed. Responsive grid adaptivity, hamburger navigation engages. |
| **Desktop 1366px / 1920px** | Laptop and widescreen monitor test | ✅ Passed. Balanced layout, 3D card tilt, luxury typography spacing. |
| **Console Errors** | Browser Developer Tools inspection | ✅ Passed. Zero JavaScript errors, zero missing assets. |

---

## 7. Compliance Statement

- **Frameworks Used:** NONE (Zero React, Next.js, Bootstrap, Tailwind, etc.)
- **External Dependencies:** NONE (Standard Google Fonts for typography; all graphics/logos are 100% self-contained local SVG files)
- **Role Compliance:** Member 4 assigned pages ONLY (**User Profile**, **Offers**, **Cinemas**, plus unifying **Landing Hub**).
