# 🛍️ Amazon Clone 

A **responsive** built with vanilla HTML, CSS, and JavaScript. This project replicates the core functionality and design of Amazon, featuring a modern UI/UX experience that works seamlessly across all devices.

---

## 📋 Table of Contents
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Pages & Navigation](#-pages--navigation)
- [Technology Stack](#-technology-stack)
- [Design & Responsiveness](#-design--responsiveness)
- [JavaScript Functionality](#-javascript-functionality)
- [Getting Started](#-getting-started)
- [Key Components](#-key-components)
- [UI/UX Highlights](#-uiux-highlights)
- [How It Works](#-how-it-works)


---

## ✨ Features

### 🎯 Core Features
- ✅ **Responsive Design** - Optimized for mobile, tablet, and desktop
- ✅ **Product Showcase** - Browse products with detailed information
- ✅ **Shopping Cart** - Add/remove items, manage quantities
- ✅ **User Authentication** - Sign In & Sign Up pages
- ✅ **Product Details** - Comprehensive product pages with specifications
- ✅ **Smooth Navigation** - Seamless page-to-page transitions
- ✅ **Interactive Elements** - Hover effects, transitions, and animations
- ✅ **Mobile-First Approach** - Touch-friendly buttons and layouts

---

## 📁 Project Structure

```
amazone-clone/
│
├── index.html              # Homepage with product sliders
├── product.html            # Product details page
├── cart.html               # Shopping cart page
├── signin.html             # User sign-in page
├── signup.html             # User registration page
│
├── style.css               # Main stylesheet (navigation, layout)
├── product.css             # Product page styles
├── cart.css                # Cart page styles
├── signin.css              # Authentication pages styles
│
├── script.js               # Main JavaScript functionality
│
├── assets/                 # Image assets folder
│   ├── amazon_logo.png
│   ├── amazon_logo_dark.png
│   ├── product_img.jpg
│   ├── header1.jpg to header6.jpg
│   ├── product1-1.jpg to product2-11.jpg
│   ├── box1-1.jpg to box3-4.jpg
│   ├── icons (dropdown, search, cart, location, etc.)
│   └── [other assets]
│
└── README.md               # Project documentation
```

---

## 🔗 Pages & Navigation

### **1. Homepage (index.html)**
- **Navigation Bar** - Logo, search, cart, sign-in
- **Product Sliders** - Multiple product carousels
- **Category Boxes** - Visual category cards (Grooming, Devices, Fashion, etc.)
- **Featured Deals** - "Deals Under $25" section
- **Footer** - Copyright information

### **2. Product Page (product.html)**
- **Product Gallery** - Main image + thumbnail navigation
- **Product Details** - Title, price, ratings, reviews
- **Color Selection** - Multiple color options
- **Purchase Section** - Add to cart, Buy Now buttons
- **Related Products** - Suggested similar items
- **Breadcrumb Navigation** - Category path (Video Games > PC > Headset)

### **3. Shopping Cart (cart.html)**
- **Cart Items** - List of added products
- **Item Management** - Quantity selector, delete, save for later
- **Cart Summary** - Subtotal and item count
- **Checkout Section** - FREE shipping info, proceed to checkout
- **Product Specs** - Style, Size, Color specifications

### **4. Sign In Page (signin.html)**
- **Login Form** - Email/mobile & password input
- **Continue Button** - Submission action
- **Help Section** - "Need help?" link
- **Sign Up Option** - Link to create new account
- **Footer Links** - Terms, Privacy, Help

### **5. Sign Up Page (signup.html)**
- **Registration Form** - Name, email/mobile, password
- **Business Option** - Link to Amazon Business
- **Account Creation** - New user registration
- **Login Link** - Redirect to sign-in page

---

## 💻 Technology Stack

| Technology | Purpose |
|-----------|---------|
| **HTML5** | Semantic structure & content |
| **CSS3** | Styling, flexbox, grid, animations |
| **JavaScript (ES6)** | Interactivity & dynamic features |
| **Responsive Design** | Mobile-first approach |

---

## 📱 Design & Responsiveness

### **Breakpoints Used**
```css
/* Desktop (1200px+) */
- Full navigation with all elements visible
- Multi-column layouts
- Hover effects enabled

/* Tablet (900px and below) */
.cart { flex-wrap: wrap; }
.box-col { max-width: 48%; }
.nav-search { min-width: 300px; }

/* Mobile (600px and below) */
- Collapsed navigation menu
- Single column layouts
- Touch-optimized buttons
- Hidden elements for space
- Responsive images & text
```

### **Mobile Optimizations**
- 🎯 Large touch targets (minimum 32px buttons)
- 📏 Flexible typography (font sizes adjust)
- 🖼️ Optimized images (responsive sizing)
- ⚡ Fast load times
- 🎨 Full-width layouts
- ✋ No hover-dependent elements on mobile

---

## 🎮 JavaScript Functionality

### **1. Image Slider (Homepage)**
```javascript
// Navigate through hero header images
const imgs = document.querySelectorAll('.header-slider ul img');
const prev_btn = document.querySelector('.control_prev');
const next_btn = document.querySelector('.control_next');

prev_btn.addEventListener('click', () => {
    // Navigate to previous image
});

next_btn.addEventListener('click', () => {
    // Navigate to next image
});
```
**Features:**
- ⏮️ Previous button (goes to last image at start)
- ⏭️ Next button (loops back to first after last)
- 🖼️ Smooth image transitions
- 📍 Only one image displayed at a time

### **2. Product Carousel (Horizontal Scroll)**
```javascript
const scrollContainer = document.querySelectorAll('.products');
for (const item of scrollContainer) {
    item.addEventListener('wheel', (evt) => {
        evt.preventDefault();
        item.scrollLeft += evt.deltaY;
    });
}
```
**Features:**
- 🎡 Mouse wheel scrolling support
- 📦 Multiple carousel on single page
- ↔️ Smooth horizontal scrolling
- 🔄 Works on all product sliders

---

## 🚀 Getting Started

### **1. Clone Repository**
```bash
git clone https://github.com/rudra610prakash-code/amazone-clone.git
cd amazone-clone
```

### **2. File Structure Setup**
Ensure all files are in the correct locations:
- HTML files in root directory
- CSS files in root directory
- JavaScript file in root directory
- Assets in `/assets` folder

### **3. Run the Project**
```bash
# Option 1: Open directly in browser
- Right-click index.html → Open with Browser

# Option 2: Use Live Server (VS Code Extension)
- Install "Live Server" extension
- Right-click index.html → Open with Live Server
```

### **4. Access Pages**
- **Homepage:** `index.html` (or `/`)
- **Product:** `/product.html`
- **Cart:** `/cart.html`
- **Sign In:** `/signin.html`
- **Sign Up:** `/signup.html`

---

## 🎨 Key Components

### **Navigation Bar**
```html
<nav>
  - Amazon Logo (links to homepage)
  - Delivery Location selector
  - Search bar with category dropdown
  - Language selector
  - Sign In link
  - Account & Lists menu
  - Orders
  - Shopping Cart icon
</nav>
```

### **Product Card**
```html
<div class="product-card">
  - Product Image
  - Discount badge (27% off)
  - Price with original
  - Product title
  - Deal indicator
</div>
```

### **Add to Cart Button**
- **Location:** Product page (primary action)
- **Color:** Bright yellow (#ffd814)
- **Hover State:** Darker gold (#ebc712)
- **Action:** Visual feedback on click
- **Mobile:** Full-width for touch targets

### **Checkout Button**
- **Location:** Cart page sidebar
- **Text:** "Proceed to checkout"
- **Styling:** Prominent yellow button
- **Responsive:** Expands on mobile

---

## 💡 UI/UX Highlights

### **Design Principles**
1. **Visual Hierarchy** - Important elements stand out
2. **Consistency** - Same colors, fonts, spacing throughout
3. **Accessibility** - High contrast, readable text
4. **User Feedback** - Hover effects, transitions
5. **Simplicity** - Clean, uncluttered interface

### **Color Scheme**
| Element | Color | Hex Code |
|---------|-------|----------|
| Primary Background | Dark Blue | #131921 |
| Navigation | Dark Gray | #232f3e |
| Accent Button | Yellow | #ffd814 |
| Text | White/Dark Gray | #fff / #565656 |
| Links | Amazon Blue | #007185 |
| Success (Stock) | Green | #007600 |
| Discount | Dark Red | #be0b3b |

### **Typography**
- **Font Family:** Outfit (imported from Google Fonts)
- **Navigation:** 14px, Bold
- **Headings:** 25-28px
- **Body Text:** 13-15px
- **Mobile:** Sizes adjust for readability

### **Interactive Elements**
- ✨ Button hover effects (color change)
- 🔗 Link underlines on hover
- ⌨️ Input focus states (blue outline)
- 🎯 Cursor pointer on clickable elements
- 📊 Product image hover effects

---

## 🔄 How It Works

### **Navigation Flow**
```
Homepage (index.html)
    ↓
[Browse Products] → Click Product → Product Page (product.html)
    ↓
[Add to Cart] → Cart Page (cart.html)
    ↓
[Proceed to Checkout] → Checkout (placeholder)

[Sign In] → Sign In Page (signin.html)
    ↓
[New User?] → Sign Up Page (signup.html)
```

### **Page Linking Strategy**

**1. HTML Anchor Links**
```html
<!-- Homepage to Product -->
<a href="/product.html">
    <img src="/assets/product_img.jpg">
</a>

<!-- Navigation to Cart -->
<a href="/cart.html" class="nav-cart">
    Cart
</a>

<!-- Sign In Page -->
<a href="/signin.html">Hello, Sign in</a>

<!-- Sign Up Link -->
<a href="/signup.html">Create your Amazon account</a>
```

**2. Logo Navigation**
```html
<!-- Return to Homepage from any page -->
<a href="/">
    <img src="assets/amazon_logo.png" width="100" alt="">
</a>
```

**3. Relative Paths**
- **Root path:** `/` links to index.html
- **File paths:** `/product.html`, `/cart.html`
- **Asset paths:** `/assets/image.jpg`

### **JavaScript Event Handling**

**1. Slider Navigation**
```javascript
prev_btn.addEventListener('click', () => {
    // Update image index
    // Display new image
});
```

**2. Product Carousel Scroll**
```javascript
item.addEventListener('wheel', (evt) => {
    evt.preventDefault();
    item.scrollLeft += evt.deltaY;
});
```

---

## 👨‍💻 Author

**Rudra Prakash**
- GitHub: [@rudra610prakash-code](https://github.com/rudra610prakash-code)


