# PRE Chiropractic Landing Page - Maintenance & Customization Guide

## Table of Contents
1. [Overview](#overview)
2. [Section 1: Updating Text and Tailwind CSS Classes](#section-1-updating-text-and-tailwind-css-classes)
3. [Section 2: Fixing Broken Links](#section-2-fixing-broken-links)
4. [Section 3: Linking Privacy and Terms Pages](#section-3-linking-privacy-and-terms-pages)
5. [Troubleshooting Guide](#troubleshooting-guide)
6. [Best Practices](#best-practices)

---

## Overview

This landing page for PRE Chiropractic is built using:
- **HTML**: The structure and content
- **Tailwind CSS**: A utility-first CSS framework for styling
- **Font Awesome**: Icons for visual enhancement
- **Vanilla JavaScript**: Interactivity (mobile menu, FAQ accordion)

The page is divided into several key sections:
- **Header & Navigation** (sticky at top)
- **Hero Section** (main welcome area)
- **Features Section** (three main service offerings)
- **Benefits Section** (four detailed benefits)
- **About Us Section**
- **Testimonials Section** (four customer reviews)
- **CTA Section** (call-to-action with background image)
- **FAQ Section** (expandable questions and answers)
- **Contact Section**
- **Footer** (links and company info)

---

## Section 1: Updating Text and Tailwind CSS Classes

### Understanding the Structure

Before making changes, it's important to understand how the page is organized. Each section is wrapped in `<section>` tags with an `id` attribute. Text content is inside tags like `<h1>`, `<h2>`, `<p>`, etc.

**Example structure:**
```html
<section id="features" class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-800/50 border-y border-gray-700">
    <h2 class="text-4xl sm:text-5xl font-bold">Your text here</h2>
    <p class="text-xl text-gray-400">Your paragraph here</p>
</section>
```

### Key Sections to Update

#### 1. **Header Logo and Navigation Text**

**Location:** Lines 41-49 (Header Navigation)

**Current code:**
```html
<span class="text-xl font-bold text-white hidden sm:inline">PRE Chiropractic</span>
```

**To change the company name:**
1. Find the line with `PRE Chiropractic`
2. Replace `PRE Chiropractic` with your company name
3. Keep all the class names exactly the same

**Example:**
```html
<span class="text-xl font-bold text-white hidden sm:inline">Your Company Name</span>
```

**Navigation menu items:** Lines 52-57

**Current code:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Benefits</a>
```

**To update menu text:**
- Change the text between `>` and `</a>` (e.g., "Features" → "Our Services")
- **Do not change** the `href="#features"` part—this links to sections
- Keep all class names unchanged

---

#### 2. **Hero Section (Main Welcome Area)**

**Location:** Lines 80-120

This is the first large section visitors see. It contains:
- Main heading
- Subheading
- Call-to-action buttons
- Statistics boxes

**Main Heading (H1):**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Your Path to Healing After an <span class="gradient-text">Oakland Collision</span>
</h1>
```

**To update:**
1. Replace `Your Path to Healing After an` with your main message
2. Keep `<span class="gradient-text">Oakland Collision</span>` if you want the gradient effect on specific words
3. Or replace the entire text inside the `<h1>` tags

**Example:**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tight mb-6 leading-tight">
    Transform Your Health with <span class="gradient-text">Expert Chiropractic Care</span>
</h1>
```

**Subheading (Paragraph):**
```html
<p class="text-xl sm:text-2xl text-gray-300 mb-8 max-w-3xl mx-auto leading-relaxed">
    Dedicated to complete recovery and well-being for car accident victims...
</p>
```

**To update:**
- Replace the text between `>` and `</p>`
- Keep the class names unchanged

---

#### 3. **Statistics Boxes**

**Location:** Lines 130-150

These three boxes show "500+ Patients Recovered", "15+ Years Experience", and "98% Patient Satisfaction"

**Current code example:**
```html
<div class="text-4xl font-bold gradient-text mb-2">500+</div>
<p class="text-gray-400 font-medium">Patients Recovered</p>
```

**To update:**
1. Change `500+` to your number
2. Change `Patients Recovered` to your statistic label
3. Keep all class names the same

**Tailwind Class Explanation:**
- `text-4xl` = Large text size
- `font-bold` = Bold font weight
- `gradient-text` = Blue-to-purple gradient color effect
- `text-gray-400` = Medium gray color
- `font-medium` = Medium font weight

---

#### 4. **Features Section**

**Location:** Lines 153-230

This section has three feature cards. Each card contains:
- An icon
- A heading
- Description text
- A bullet-point list

**Feature Card Structure:**
```html
<div class="card-hover bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-lg p-8 hover:border-blue-500 transition-all duration-300">
    <div class="w-14 h-14 bg-gradient-to-br from-blue-500 to-blue-600 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-leaf text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Holistic Approach to Healing</h3>
    <p class="text-gray-400 leading-relaxed mb-6">Description text...</p>
    <ul class="space-y-3 text-gray-300">
        <li class="flex items-center gap-3">
            <i class="fas fa-check-circle text-blue-500"></i>
            <span>Bullet point text</span>
        </li>
    </ul>
</div>
```

**To update the heading:**
```html
<h3 class="text-2xl font-bold mb-4">Your New Feature Title</h3>
```

**To update the description:**
```html
<p class="text-gray-400 leading-relaxed mb-6">Your new description text goes here...</p>
```

**To update bullet points:**
```html
<li class="flex items-center gap-3">
    <i class="fas fa-check-circle text-blue-500"></i>
    <span>Your new bullet point text</span>
</li>
```

**To change the icon:**
1. Go to [Font Awesome Icons](https://fontawesome.com/icons)
2. Search for an icon you want
3. Copy the icon name (e.g., "fa-heart", "fa-star")
4. Replace `fa-leaf` with your new icon name

**Example:** Change from leaf to heart:
```html
<!-- Before -->
<i class="fas fa-leaf text-white text-2xl"></i>

<!-- After -->
<i class="fas fa-heart text-white text-2xl"></i>
```

**Understanding Tailwind Classes in Features:**
- `bg-gradient-to-br` = Background gradient from top-left to bottom-right
- `from-gray-800 to-gray-900` = Gradient colors (light gray to dark gray)
- `border border-gray-700` = Border with gray color
- `rounded-lg` = Rounded corners
- `p-8` = Padding (space inside) of 8 units
- `hover:border-blue-500` = Border turns blue when you hover over it
- `transition-all duration-300` = Smooth animation over 300 milliseconds

---

#### 5. **Benefits Section**

**Location:** Lines 233-360

This section has four benefits, each with:
- An icon box
- A heading
- Description text
- A bullet-point list

**Structure is similar to features, but laid out differently:**
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-16 w-16 rounded-lg bg-gradient-to-br from-blue-500 to-blue-600">
            <i class="fas fa-heartbeat text-white text-2xl"></i>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold mb-3">Improved Long-Term Health</h3>
        <p class="text-gray-400 leading-relaxed mb-4">Description...</p>
        <ul class="space-y-2 text-gray-300">
            <li class="flex items-center gap-2">
                <i class="fas fa-arrow-right text-blue-500"></i>
                <span>Bullet point</span>
            </li>
        </ul>
    </div>
</div>
```

**To update:**
- Change heading text in `<h3>` tags
- Change description in `<p>` tags
- Change bullet points in `<span>` tags inside `<li>` tags
- Change icons using Font Awesome names

---

#### 6. **About Us Section**

**Location:** Lines 363-430

**Main heading:**
```html
<h2 class="text-4xl sm:text-5xl font-bold tracking-tight mb-8">
    About <span class="gradient-text">PRE Chiropractic</span>
</h2>
```

**Paragraphs:**
```html
<p class="text-lg text-gray-400 leading-relaxed mb-6">
    Your company story and information...
</p>
```

**To update:**
- Replace company name and story text
- Keep class names unchanged
- The `<span class="gradient-text">` creates the gradient effect on specific words

---

#### 7. **Testimonials Section**

**Location:** Lines 449-510

Each testimonial card shows:
- Star rating
- Quote text
- Customer name and title

**Testimonial card structure:**
```html
<div class="card-hover bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-lg p-6 hover:border-blue-500 transition-all duration-300">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 leading-relaxed mb-6">
        "Customer quote text..."
    </p>
    <div class="border-t border-gray-700 pt-4">
        <p class="font-semibold text-white">Sarah Mitchell</p>
        <p class="text-gray-400 text-sm">Oakland, CA</p>
    </div>
</div>
```

**To update:**
- Change quote text in the `<p>` with the quote
- Change customer name in the first `<p>` after the border
- Change location/title in the second `<p>` after the border
- To change star rating, add or remove `<i class="fas fa-star text-yellow-400"></i>` lines

---

#### 8. **FAQ Section**

**Location:** Lines 553-650

Each FAQ item has a question and answer that expands/collapses.

**FAQ item structure:**
```html
<div class="faq-item bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-lg overflow-hidden hover:border-blue-500 transition-colors duration-300">
    <button class="faq-question w-full px-6 py-6 text-left flex items-center justify-between cursor-pointer hover:bg-gray-800/50 transition-colors duration-300">
        <span class="text-lg font-semibold text-white flex items-center gap-3">
            <i class="fas fa-question-circle text-blue-500"></i>
            Your question text here?
        </span>
        <i class="faq-icon fas fa-chevron-down text-gray-400 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 pb-6 border-t border-gray-700 bg-gray-900/50">
        <p class="text-gray-300 leading-relaxed">
            Your answer text here...
        </p>
    </div>
</div>
```

**To update:**
- Change question text in the `<span>` after the icon
- Change answer text in the `<p>` inside the `faq-answer` div
- Keep the `class="hidden"` on the `faq-answer` div—JavaScript handles showing/hiding
- Keep the `class="faq-question"` and `class="faq-answer"` classes—JavaScript needs these

---

#### 9. **Footer**

**Location:** Lines 700-800

The footer contains:
- Company info
- Quick links
- Resources
- Contact information
- Social media links
- Copyright

**Company name in footer:**
```html
<span class="text-xl font-bold text-white">PRE Chiropractic</span>
```

**Company description:**
```html
<p class="text-gray-400 leading-relaxed">
    Dedicated to complete recovery and well-being for Oakland collision victims...
</p>
```

**Quick links section:**
```html
<li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
```

**Contact email:**
```html
<a href="mailto:prechiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">prechiropractic@gmail.com</a>
```

**To update:**
- Change company name
- Change description text
- Change email address (in both `href="mailto:"` and visible text)
- Change location text
- Update copyright year

---

### Understanding Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here are the most common ones used in this landing page:

| Class | Purpose | Example |
|-------|---------|---------|
| `text-4xl` | Font size (4xl = very large) | `text-sm`, `text-lg`, `text-2xl`, `text-5xl` |
| `font-bold` | Font weight (bold) | `font-light`, `font-normal`, `font-semibold` |
| `text-white` | Text color (white) | `text-gray-300`, `text-blue-500`, `text-purple-600` |
| `bg-gray-900` | Background color (dark gray) | `bg-blue-500`, `bg-gradient-to-br` |
| `p-8` | Padding (space inside) | `p-4`, `p-6`, `p-12` |
| `px-4` | Padding left and right | `py-6`, `px-8` |
| `mb-6` | Margin bottom (space below) | `mt-4`, `ml-3`, `mr-8` |
| `rounded-lg` | Rounded corners | `rounded-full`, `rounded-md` |
| `border` | Border around element | `border-2`, `border-gray-700` |
| `hover:text-white` | Style when hovering | `hover:bg-blue-500`, `hover:scale-105` |
| `transition-all` | Smooth animation | `transition-colors`, `duration-300` |
| `hidden` | Hide element | `block`, `flex`, `inline` |
| `flex` | Display as flexbox | `grid`, `inline-block` |
| `gap-4` | Space between flex items | `gap-6`, `gap-8` |

**Responsive classes** (change based on screen size):
- `sm:` = Small screens (640px+)
- `md:` = Medium screens (768px+)
- `lg:` = Large screens (1024px+)

**Example:**
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl">
    <!-- On small screens: text-4xl (large) -->
    <!-- On medium screens: text-5xl (larger) -->
    <!-- On large screens: text-6xl (largest) -->
</h1>
```

---

### Changing Colors

The page uses a color scheme of blues, purples, and grays. To change colors:

**Blue elements:**
- Change `blue-500` or `blue-600` to another color
- Available colors: `red`, `yellow`, `green`, `cyan`, `pink`, `indigo`, etc.
- Available shades: `50`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`

**Example - Change blue to green:**
```html
<!-- Before -->
<div class="bg-blue-500">Button</div>

<!-- After -->
<div class="bg-green-500">Button</div>
```

**Gradient colors:**
```html
<!-- Current gradient (blue to purple) -->
<div class="bg-gradient-to-r from-blue-500 to-purple-600">

<!-- Change to green to teal -->
<div class="bg-gradient-to-r from-green-500 to-teal-600">
```

---

## Section 2: Fixing Broken Links

### Understanding Links in This Page

Links are created with `<a>` tags. The `href` attribute tells the browser where to go when clicked.

**Types of links on this page:**
1. **Internal anchor links** - Jump to sections on the same page (e.g., `#features`)
2. **External links** - Go to other websites (e.g., scheduling app)
3. **Email links** - Open email client (e.g., `mailto:email@example.com`)
4. **Page links** - Go to other HTML files (e.g., `privacy.html`)

---

### All Links in the Current Page

#### Navigation Links (Header)

**Location:** Lines 52-57 (Desktop menu) and Lines 62-69 (Mobile menu)

```html
<!-- Desktop Navigation -->
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="...">Schedule Now</a>
```

**Status:** ✅ These links are correct if you want to keep the current scheduling service.

**To change the scheduling link:**
1. Find both instances (desktop and mobile menu)
2. Replace the entire URL in `href=""`
3. Keep the text and classes the same

**Example:**
```html
<!-- Before -->
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735">Schedule Now</a>

<!-- After (if using different scheduling service) -->
<a href="https://calendly.com/yourname">Schedule Now</a>
```

---

#### Hero Section Buttons

**Location:** Lines 112-119

```html
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="...">
    <i class="fas fa-calendar-check"></i> Book Your Consultation
</a>
<a href="#features" class="...">
    <i class="fas fa-arrow-down"></i> Learn More
</a>
```

**Status:**
- First button: External link to scheduling (correct if using Acuity)
- Second button: Internal anchor to Features section (correct)

---

#### CTA Section Buttons

**Location:** Lines 512-520

```html
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="...">
    <i class="fas fa-phone"></i> Schedule Consultation
</a>
<a href="mailto:prechiropractic@gmail.com" class="...">
    <i class="fas fa-envelope"></i> Send Inquiry
</a>
```

**Status:**
- First button: External scheduling link (update if needed)
- Second button: Email link (update email address)

**To change email:**
```html
<!-- Before -->
<a href="mailto:prechiropractic@gmail.com">Send Inquiry</a>

<!-- After -->
<a href="mailto:youremail@yourcompany.com">Send Inquiry</a>
```

---

#### Contact Section

**Location:** Lines 656-665

```html
<a href="mailto:prechiropractic@gmail.com" class="...">
    <i class="fas fa-envelope"></i>
    prechiropractic@gmail.com
</a>
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="...">
    <i class="fas fa-calendar-check"></i>
    Schedule Now
</a>
```

**Status:**
- Email link: Update email address
- Scheduling link: Update if using different service

---

#### Footer Links

**Location:** Lines 700-800

**Quick Links section (Lines 722-729):**
```html
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
```

**Status:** ✅ These are correct (internal anchors)

---

**Resources section (Lines 734-741):**
```html
<a href="privacy.html" class="...">Privacy Policy</a>
<a href="terms.html" class="...">Terms of Service</a>
<a href="blog.html" class="...">Blog</a>
<a href="mailto:prechiropractic@gmail.com" class="...">Contact</a>
```

**Status:** ⚠️ These files may not exist yet:
- `privacy.html` - Needs to be created
- `terms.html` - Needs to be created
- `blog.html` - Needs to be created
- Email link - Update email address

---

**Contact Info section (Lines 746-760):**
```html
<a href="mailto:prechiropractic@gmail.com" class="...">prechiropractic@gmail.com</a>
```

**Status:** ⚠️ Update email address

```html
<span class="...">Oakland, California</span>
```

**To update location:**
```html
<span class="...">Your City, Your State</span>
```

---

**Social Links (Lines 766-786):**
```html
<a href="#" class="...">
    <i class="fab fa-facebook-f"></i>
</a>
<a href="#" class="...">
    <i class="fab fa-twitter"></i>
</a>
<a href="#" class="...">
    <i class="fab fa-instagram"></i>
</a>
<a href="#" class="...">
    <i class="fab fa-linkedin-in"></i>
</a>
```

**Status:** ⚠️ These are placeholder links (`href="#"`)

**To update social media links:**
1. Replace `href="#"` with your actual social media URL
2. Keep the icon and classes the same

**Example:**
```html
<!-- Before -->
<a href="#" class="..." aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- After -->
<a href="https://facebook.com/yourpage" class="..." aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

---

### Complete Link Update Checklist

Use this checklist to find and update all links:

**Scheduling/Booking Links:**
- [ ] Line 58: Desktop menu "Schedule Now"
- [ ] Line 67: Mobile menu "Schedule Now"
- [ ] Line 113: Hero "Book Your Consultation"
- [ ] Line 514: CTA "Schedule Consultation"
- [ ] Line 661: Contact "Schedule Now"

**Email Links:**
- [ ] Line 515: CTA "Send Inquiry"
- [ ] Line 657: Contact email link
- [ ] Line 757: Footer email link
- [ ] Line 740: Footer "Contact" link

**Page Links (To create later):**
- [ ] Line 735: Privacy Policy
- [ ] Line 736: Terms of Service
- [ ] Line 737: Blog

**Social Media Links:**
- [ ] Line 767: Facebook
- [ ] Line 772: Twitter
- [ ] Line 777: Instagram
- [ ] Line 782: LinkedIn

---

### How to Update a Link - Step by Step

**Example: Update the email address**

1. **Find the email link** - Search for `prechiropractic@gmail.com` in your code editor
2. **Identify what to change:**
   - In `href="mailto:prechiropractic@gmail.com"` - Change the email address
   - In visible text `prechiropractic@gmail.com` - Also change this
3. **Replace both instances:**

```html
<!-- Before -->
<a href="mailto:prechiropractic@gmail.com" class="...">
    <i class="fas fa-envelope"></i>
    prechiropractic@gmail.com
</a>

<!-- After -->
<a href="mailto:youremail@company.com" class="...">
    <i class="fas fa-envelope"></i>
    youremail@company.com
</a>
```

4. **Save the file**
5. **Test the link** - Open the page in a browser and click the link

---

### Example: Update Scheduling Link

The scheduling link appears in multiple places. Here's how to update all of them:

**Step 1: Find your scheduling service URL**
- If using Acuity Scheduling: Keep the current URL or get your new one
- If using Calendly: Get your Calendly URL (e.g., `https://calendly.com/yourname`)
- If using other service: Get your booking URL

**Step 2: Update each instance**

```html
<!-- Desktop Menu (Line 58) -->
<a href="https://your-new-scheduling-url.com" class="...">Schedule Now</a>

<!-- Mobile Menu (Line 67) -->
<a href="https://your-new-scheduling-url.com" class="...">Schedule Now</a>

<!-- Hero Section (Line 113) -->
<a href="https://your-new-scheduling-url.com" class="...">
    <i class="fas fa-calendar-check"></i> Book Your Consultation
</a>

<!-- CTA Section (Line 514) -->
<a href="https://your-new-scheduling-url.com" class="...">
    <i class="fas fa-phone"></i> Schedule Consultation
</a>

<!-- Contact Section (Line 661) -->
<a href="https://your-new-scheduling-url.com" class="...">
    <i class="fas fa-calendar-check"></i>
    Schedule Now
</a>
```

---

### Example: Update Social Media Links

**Step 1: Get your social media URLs**
- Facebook: `https://facebook.com/yourpage`
- Twitter/X: `https://twitter.com/yourhandle`
- Instagram: `https://instagram.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`

**Step 2: Update the links (Lines 767-782)**

```html
<!-- Before -->
<a href="#" class="..." aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- After -->
<a href="https://facebook.com/yourpage" class="..." aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

---

## Section 3: Linking Privacy and Terms Pages

### Understanding Page Structure

Currently, the footer has links to three pages that don't exist yet:
- `privacy.html` (Privacy Policy)
- `terms.html` (Terms of Service)
- `blog.html` (Blog - optional)

This section explains how to create these files and link them properly.

---

### Step 1: Create the Privacy Policy Page

**Step 1a: Create a new file**

1. Open your code editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 1b: Add basic HTML structure**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for PRE Chiropractic">
    <title>Privacy Policy | PRE Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header (Copy from index.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heart text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">PRE Chiropractic</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                <a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="bg-gradient-to-r from-blue-500 to-purple-600 hover:shadow-lg hover:shadow-purple-500/50 text-white px-6 py-2 rounded-lg font-semibold transition-all duration-300 hover:scale-105">Schedule Now</a>
            </div>
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300">
                <i class="fas fa-bars text-white text-xl"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl font-bold mb-12">Privacy Policy</h1>
            
            <div class="space-y-8 text-gray-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Introduction</h2>
                    <p class="leading-relaxed">
                        At PRE Chiropractic, we are committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Information We Collect</h2>
                    <p class="leading-relaxed mb-4">
                        We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you choose to participate in various activities related to the Site.</li>
                        <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                        <li>Data From Third Parties: Information received from third parties, including but not limited to business contact information.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Use of Your Information</h2>
                    <p class="leading-relaxed mb-4">
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Process your transactions and send related information</li>
                        <li>Email you regarding your account or order</li>
                        <li>Fulfill and manage your requests</li>
                        <li>Generate a personal profile about you so that future visits to the Site will be personalized</li>
                        <li>Increase the efficiency and operation of the Site</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Disclosure of Your Information</h2>
                    <p class="leading-relaxed">
                        We may share information we have collected about you in certain situations:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4 mt-4">
                        <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information is necessary to comply with the law.</li>
                        <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us, including payment processing, data analysis, email delivery, hosting services, customer service, and marketing assistance.</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Security of Your Information</h2>
                    <p class="leading-relaxed">
                        We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or method of electronic storage is 100% secure.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">Contact Us</h2>
                    <p class="leading-relaxed">
                        If you have questions or comments about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:prechiropractic@gmail.com" class="text-blue-400 hover:text-blue-300">prechiropractic@gmail.com</a><br>
                        <strong>Location:</strong> Oakland, California
                    </p>
                </div>

                <div class="mt-12 p-6 bg-gray-800 rounded-lg border border-gray-700">
                    <p class="text-sm text-gray-400">
                        Last Updated: January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Copy from index.html) -->
    <footer class="bg-gray-800 border-t border-gray-700 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-heart text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">PRE Chiropractic</span>
                    </div>
                    <p class="text-gray-400 leading-relaxed">
                        Dedicated to complete recovery and well-being for Oakland collision victims.
                    </p>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Quick Links</h3>
                    <ul class="space-y-3">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Resources</h3>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
                        <li><a href="mailto:prechiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Contact Info</h3>
                    <ul class="space-y-4">
                        <li class="flex items-start gap-3">
                            <i class="fas fa-envelope text-blue-500 mt-1 flex-shrink-0"></i>
                            <a href="mailto:prechiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">prechiropractic@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fas fa-map-marker-alt text-blue-500 mt-1 flex-shrink-0"></i>
                            <span class="text-gray-400">Oakland, California</span>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 pt-8 text-center">
                <p class="text-gray-400">
                    &copy; 2025 PRE Chiropractic. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            if (mobileMenuButton) {
                mobileMenuButton.addEventListener('click', () => {
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

---

### Step 2: Create the Terms of Service Page

**Step 2a: Create a new file**

1. Create a new file
2. Save it as `terms.html` in the same folder as `index.html`

**Step 2b: Add basic HTML structure**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for PRE Chiropractic">
    <title>Terms of Service | PRE Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header (Same as privacy.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heart text-white text-lg"></i>
                </div>
                <span class="text-xl font-bold text-white hidden sm:inline">PRE Chiropractic</span>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">FAQ</a>
                <a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" class="bg-gradient-to-r from-blue-500 to-purple-600 hover:shadow-lg hover:shadow-purple-500/50 text-white px-6 py-2 rounded-lg font-semibold transition-all duration-300 hover:scale-105">Schedule Now</a>
            </div>
            <button class="md:hidden mobile-menu-button p-2 rounded-lg hover:bg-gray-800 transition-colors duration-300">
                <i class="fas fa-bars text-white text-xl"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl font-bold mb-12">Terms of Service</h1>
            
            <div class="space-y-8 text-gray-300">
                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Agreement to Terms</h2>
                    <p class="leading-relaxed">
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p class="leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on PRE Chiropractic's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p class="leading-relaxed">
                        The materials on PRE Chiropractic's website are provided on an 'as is' basis. PRE Chiropractic makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p class="leading-relaxed">
                        In no event shall PRE Chiropractic or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on PRE Chiropractic's website, even if PRE Chiropractic or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p class="leading-relaxed">
                        The materials appearing on PRE Chiropractic's website could include technical, typographical, or photographic errors. PRE Chiropractic does not warrant that any of the materials on its website are accurate, complete, or current. PRE Chiropractic may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p class="leading-relaxed">
                        PRE Chiropractic has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by PRE Chiropractic of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p class="leading-relaxed">
                        PRE Chiropractic may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p class="leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of California, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div>
                    <h2 class="text-2xl font-bold text-white mb-4">9. Contact Information</h2>
                    <p class="leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Email:</strong> <a href="mailto:prechiropractic@gmail.com" class="text-blue-400 hover:text-blue-300">prechiropractic@gmail.com</a><br>
                        <strong>Location:</strong> Oakland, California
                    </p>
                </div>

                <div class="mt-12 p-6 bg-gray-800 rounded-lg border border-gray-700">
                    <p class="text-sm text-gray-400">
                        Last Updated: January 2025
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Same as privacy.html) -->
    <footer class="bg-gray-800 border-t border-gray-700 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-blue-500 to-purple-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-heart text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">PRE Chiropractic</span>
                    </div>
                    <p class="text-gray-400 leading-relaxed">
                        Dedicated to complete recovery and well-being for Oakland collision victims.
                    </p>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Quick Links</h3>
                    <ul class="space-y-3">
                        <li><a href="index.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Resources</h3>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
                        <li><a href="mailto:prechiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-lg font-semibold text-white mb-6">Contact Info</h3>
                    <ul class="space-y-4">
                        <li class="flex items-start gap-3">
                            <i class="fas fa-envelope text-blue-500 mt-1 flex-shrink-0"></i>
                            <a href="mailto:prechiropractic@gmail.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">prechiropractic@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-3">
                            <i class="fas fa-map-marker-alt text-blue-500 mt-1 flex-shrink-0"></i>
                            <span class="text-gray-400">Oakland, California</span>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 pt-8 text-center">
                <p class="text-gray-400">
                    &copy; 2025 PRE Chiropractic. All rights reserved.
                </p>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            if (mobileMenuButton) {
                mobileMenuButton.addEventListener('click', () => {
                    const icon = mobileMenuButton.querySelector('i');
                    if (icon) {
                        icon.classList.toggle('fa-bars');
                        icon.classList.toggle('fa-times');
                    }
                });
            }
        });
    </script>
</body>
</html>
```

---

### Step 3: Verify Links in index.html

The footer links in `index.html` should already point to these files. Let's verify:

**Location:** Lines 735-737 in index.html

```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
```

**Status:**
- ✅ Privacy Policy link is correct (points to `privacy.html`)
- ✅ Terms of Service link is correct (points to `terms.html`)
- ⚠️ Blog link points to `blog.html` (which doesn't exist yet)

**To remove the Blog link** (if you don't want it):

1. Find lines 737 in `index.html`
2. Delete this line:
```html
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
```

Or keep it and create a `blog.html` file later.

---

### Step 4: Update Email Addresses in Policy Pages

In both `privacy.html` and `terms.html`, replace `prechiropractic@gmail.com` with your actual email address.

**Locations to update in privacy.html:**
- Line in Contact Us section
- Line in footer contact info
- Any other instances of the email

**Locations to update in terms.html:**
- Line in Contact Information section
- Line in footer contact info
- Any other instances of the email

**Search and replace method:**
1. Use Ctrl+H (Windows) or Cmd+H (Mac) to open Find and Replace
2. Find: `prechiropractic@gmail.com`
3. Replace with: `youremail@yourcompany.com`
4. Replace all instances

---

### Step 5: File Organization

After creating these files, your folder structure should look like this:

```
your-project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy Policy)
├── terms.html          (Terms of Service)
└── blog.html           (Optional - create if needed)
```

**Important:** All HTML files must be in the same folder for the links to work correctly.

---

### Step 6: Test All Links

After creating the files, test the links:

1. **Open `index.html` in your browser**
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - Should open `privacy.html`
4. **Click on "Terms of Service"** - Should open `terms.html`
5. **From the policy pages, click "Home"** - Should return to `index.html`
6. **From the policy pages, click links in the header** - Should work correctly

---

### Adding Links from Privacy to Terms (and vice versa)

You can add links between policy pages for better navigation.

**In privacy.html footer Resources section**, add a link to Terms:
```html
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

**In terms.html footer Resources section**, add a link to Privacy:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
```

---

### Example: Complete Footer Link Section

Here's what the complete Resources section should look like in all three files:

```html
<div>
    <h3 class="text-lg font-semibold text-white mb-6">Resources</h3>
    <ul class="space-y-3">
        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
        <li><a href="index.html#faq" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">FAQ</a></li>
        <li><a href="mailto:youremail@yourcompany.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
    </ul>
</div>
```

---

## Troubleshooting Guide

### Issue 1: Links Not Working

**Problem:** Clicking a link doesn't do anything or shows a 404 error.

**Possible causes:**
1. File name is misspelled
2. File is in a different folder
3. Relative path is incorrect

**Solution:**
1. Check that all HTML files are in the same folder
2. Verify file names match exactly (including capitalization):
   - `privacy.html` (not `Privacy.html` or `privacy.HTML`)
   - `terms.html` (not `Terms.html`)
3. Check that links use correct file names:
   - `href="privacy.html"` ✅
   - `href="privacy.HTML"` ❌
   - `href="./privacy.html"` ❌ (unnecessary)

---

### Issue 2: Mobile Menu Not Working

**Problem:** Mobile menu button doesn't open the menu.

**Possible causes:**
1. JavaScript is disabled
2. JavaScript code was accidentally deleted
3. Class names were changed

**Solution:**
1. Check that JavaScript code is at the bottom of the page (before `</body>`)
2. Verify class names match:
   - `class="mobile-menu-button"` ✅
   - `class="mobile-menu"` ✅
3. Don't change these class names—JavaScript depends on them

---

### Issue 3: Styling Looks Wrong

**Problem:** Colors, spacing, or layout looks incorrect.

**Possible causes:**
1. Tailwind CSS classes were accidentally deleted
2. Class names were misspelled
3. Tailwind CDN link is broken

**Solution:**
1. Check that Tailwind CSS link is in the `<head>`:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
2. Restore any deleted class names
3. Check for typos in class names:
   - `text-gray-400` ✅
   - `text-gray-4000` ❌
   - `text-gray-` ❌

---

### Issue 4: FAQ Accordion Not Working

**Problem:** FAQ items don't expand/collapse when clicked.

**Possible causes:**
1. JavaScript code was deleted
2. Class names were changed
3. HTML structure was modified

**Solution:**
1. Verify JavaScript code is present (lines 805-845)
2. Check that class names are correct:
   - `class="faq-item"` ✅
   - `class="faq-question"` ✅
   - `class="faq-answer"` ✅
   - `class="faq-icon"` ✅
3. Don't modify the HTML structure of FAQ items

---

### Issue 5: Gradient Text Not Showing

**Problem:** Text that should have a gradient color appears as regular text.

**Possible causes:**
1. `gradient-text` class was deleted
2. Custom CSS was removed
3. Browser doesn't support gradients

**Solution:**
1. Check that custom CSS is in the `<style>` tag (lines 16-27):
```html
<style>
    .gradient-text {
        background: linear-gradient(135deg, #3b82f6 0%, #8b5cf6 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }
</style>
```
2. Ensure `<span class="gradient-text">` is used for text that should have gradient
3. Try a different browser if gradient still doesn't show

---

### Issue 6: Email Links Not Working

**Problem:** Clicking email link doesn't open email client.

**Possible causes:**
1. Email format is incorrect
2. No email client is configured on the computer
3. Browser security settings

**Solution:**
1. Verify email format:
   - `href="mailto:youremail@company.com"` ✅
   - `href="mailto:youremail@company"` ❌ (missing domain)
   - `href="youremail@company.com"` ❌ (missing mailto:)
2. Try using a different email client
3. Check browser settings for email handling

---

### Issue 7: External Links Not Working

**Problem:** Scheduling link or social media links don't work.

**Possible causes:**
1. URL is incorrect
2. Website is down
3. URL doesn't include `https://`

**Solution:**
1. Verify URL starts with `https://`:
   - `href="https://example.com"` ✅
   - `href="example.com"` ❌
2. Test the URL in a new browser tab to confirm it works
3. Check that URL is complete and correct

---

### Issue 8: Page Looks Broken on Mobile

**Problem:** Layout is messed up on mobile devices.

**Possible causes:**
1. Responsive classes were deleted
2. Viewport meta tag is missing
3. CSS was modified

**Solution:**
1. Check that viewport meta tag is in `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
2. Verify responsive classes are present:
   - `sm:text-5xl` (small screens)
   - `md:flex` (medium screens)
   - `lg:px-8` (large screens)
3. Test on actual mobile device or use browser's responsive design mode

---

### Issue 9: Text Content Not Displaying

**Problem:** Text is missing or invisible.

**Possible causes:**
1. Text color is same as background
2. Text is inside `hidden` class
3. Font size is 0

**Solution:**
1. Check text color class:
   - `text-white` ✅
   - `text-gray-900` ❌ (too dark for dark background)
2. Remove `hidden` class if text should be visible
3. Check font size class is present:
   - `text-lg` ✅
   - No size class ❌

---

### Issue 10: Images or Icons Not Showing

**Problem:** Icons from Font Awesome don't display.

**Possible causes:**
1. Font Awesome CDN link is broken
2. Icon name is incorrect
3. Icon doesn't exist

**Solution:**
1. Check Font Awesome link in `<head>`:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```
2. Verify icon name is correct:
   - `<i class="fas fa-heart"></i>` ✅
   - `<i class="fas fa-hart"></i>` ❌ (typo)
3. Check [Font Awesome documentation](https://fontawesome.com/icons) for correct icon names

---

## Best Practices

### 1. **Always Back Up Before Making Changes**

Before editing any file:
```
1. Make a copy of the original file
2. Name it something like "index-backup.html"
3. Keep it in a safe location
4. If something breaks, you can restore from backup
```

---

### 2. **Test After Each Change**

After updating any content:
```
1. Save the file
2. Refresh the browser (Ctrl+R or Cmd+R)
3. Test the change
4. Check on mobile if responsive
```

---

### 3. **Keep Class Names Intact**

**Don't change these:**
```html
<!-- Keep these class names exactly as they are -->
<div class="card-hover">...</div>
<div class="faq-item">...</div>
<button class="faq-question">...</button>
<div class="faq-answer">...</div>
<span class="gradient-text">...</span>
<button class="mobile-menu-button">...</button>
<div class="mobile-menu">...</div>
```

**These are used by CSS and JavaScript**

---

### 4. **Maintain Consistent Formatting**

Keep your code organized:
```html
<!-- Good - easy to read -->
<div class="card-hover bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-lg p-8">
    <h3 class="text-2xl font-bold mb-4">Title</h3>
    <p class="text-gray-400 leading-relaxed">Description</p>
</div>

<!-- Bad - hard to read -->
<div class="card-hover bg-gradient-to-br from-gray-800 to-gray-900 border border-gray-700 rounded-lg p-8"><h3 class="text-2xl font-bold mb-4">Title</h3><p class="text-gray-400 leading-relaxed">Description</p></div>
```

---

### 5. **Use Proper File Naming**

File names should be:
- Lowercase: `privacy.html` ✅ (not `Privacy.html`)
- No spaces: `privacy-policy.html` ✅ (not `privacy policy.html`)
- Descriptive: `about-us.html` ✅ (not `page1.html`)
- Consistent: Use hyphens for multi-word names

---

### 6. **Validate Links Regularly**

Create a checklist and test all links monthly:
```
□ Navigation menu links
□ CTA buttons
□ Footer links
□ Social media links
□ Email links
□ Policy page links
```

---

### 7. **Update Content Regularly**

Keep your website fresh:
- Update testimonials quarterly
- Refresh statistics when they change
- Update team information
- Keep contact info current
- Review and update FAQ based on common questions

---

### 8. **Monitor External Links**

External links can break if:
- Third-party website changes their URL
- Scheduling service changes
- Social media accounts are deleted

**Check monthly:**
- Scheduling link still works
- Social media links are active
- Email address is correct

---

### 9. **Use Meaningful Comments**

Add comments to help future edits:
```html
<!-- Hero Section - Main welcome area -->
<section id="hero" class="...">
    <!-- Update this heading for seasonal promotions -->
    <h1 class="...">Your seasonal message here</h1>
</section>

<!-- Features Section - Three main service offerings -->
<section id="features" class="...">
    <!-- Add or remove feature cards as needed -->
</section>
```

---

### 10. **Keep CSS and JavaScript Intact**

**Never delete:**
```html
<!-- These are essential -->
<script src="https://cdn.tailwindcss.com"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
    /* Custom CSS for gradient text and animations */
</style>
<script>
    /* JavaScript for mobile menu and FAQ accordion */
</script>
```

---

### 11. **SEO Best Practices**

When updating content, remember SEO:
- Keep titles descriptive (under 60 characters)
- Use descriptive headings (h1, h2, h3)
- Include keywords naturally
- Keep meta descriptions relevant
- Use descriptive alt text for images
- Maintain internal linking structure

---

### 12. **Accessibility Guidelines**

Make your site accessible:
```html
<!-- Always include alt text for images -->
<img src="image.jpg" alt="Descriptive text about image">

<!-- Use semantic HTML -->
<button>Click me</button>  ✅
<div onclick="...">Click me</div>  ❌

<!-- Ensure sufficient color contrast -->
<p class="text-white bg-gray-900">Good contrast ✅</p>
<p class="text-gray-500 bg-gray-400">Poor contrast ❌</p>

<!-- Use proper heading hierarchy -->
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
```

---

## Quick Reference Guide

### Most Common Updates

**Update company name:**
- Search for "PRE Chiropractic"
- Replace with your company name
- Update in: Header, Footer, About section, Meta tags

**Update email address:**
- Search for "prechiropractic@gmail.com"
- Replace with your email
- Update in: Navigation, Footer, Contact section, Policy pages

**Update phone number:**
- Add phone number in Contact section
- Add in Footer contact info
- Update in CTA buttons if needed

**Update scheduling link:**
- Find all instances of Acuity Scheduling URL
- Replace with your booking service URL
- Update in: Navigation, Hero buttons, CTA section, Contact section

**Update testimonials:**
- Find Testimonials section (line 449)
- Replace quote text
- Update customer name and location

**Update statistics:**
- Find Stats section (line 130)
- Update numbers (500+, 15+, 98%)
- Update labels

---

## Final Checklist

Before publishing your website:

- [ ] All text content is updated
- [ ] Company name is consistent
- [ ] Email addresses are correct
- [ ] Scheduling link works
- [ ] All internal links work
- [ ] All external links work
- [ ] Mobile menu works
- [ ] FAQ accordion works
- [ ] Page looks good on mobile
- [ ] Page looks good on desktop
- [ ] All images/icons display
- [ ] Testimonials are updated
- [ ] Contact information is current
- [ ] Privacy policy is created
- [ ] Terms of service is created
- [ ] Social media links are correct
- [ ] No broken links in footer
- [ ] All colors are correct
- [ ] Spacing and layout looks good
- [ ] Website has been tested in multiple browsers

---

## Conclusion

This landing page is built with modern, maintainable code that's easy to customize. By following this guide, you can:

1. **Update all text content** without breaking the design
2. **Fix broken links** and ensure proper navigation
3. **Create and link policy pages** for legal compliance
4. **Maintain professional appearance** while making changes
5. **Troubleshoot common issues** quickly

For additional help with HTML, CSS, or web development, refer to:
- [MDN Web Docs](https://developer.mozilla.org/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [W3Schools HTML Tutorial](https://www.w3schools.com/html/)

Good luck with your website maintenance and customization!