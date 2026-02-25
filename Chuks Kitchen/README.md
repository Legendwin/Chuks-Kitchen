# Chuks Kitchen - Frontend Documentation

## Project Overview

**Chuks Kitchen** is a modern, responsive web application for an authentic Nigerian restaurant delivery service. The platform showcases traditional Nigerian home-cooked meals with a focus on quality, authenticity, and customer experience.

The application provides customers with:
- **Browse & Discover**: Explore menu categories including Jollof delights, swallows & soups, grills, beverages, and desserts
- **User Authentication**: Seamless sign-up and sign-in flows with social login options
- **Order Management**: Track and manage food orders through a dedicated portal
- **Responsive Design**: Optimized experience across desktop, tablet, and mobile devices

## Tech Stack Used

### Languages & Frameworks
- **HTML5**: Semantic markup for accessibility and SEO
- **CSS3**: Advanced styling with CSS custom properties (variables), Flexbox, and Grid layouts
- **JavaScript**: (Framework ready - structure in place for progressive enhancement)

### Design Tools & Libraries
- **Google Fonts**: Inter, Jost, Island Moments, and Poppins for consistent typography
- **Font Awesome 6**: Icon library via CDN for UI elements (envelope, lock, eye, bars, etc.)
- **SVG Graphics**: Custom Search icon

### Design Rationale
- **CSS Variables**: Centralized color management for consistent branding and easy theme updates
- **Mobile-First Approach**: 
- **Semantic Structure**: Clean HTML hierarchy for maintainability and accessibility

## Project Structure

```
Chuks Kitchen/
├── README.md
├── index.html           
├── explore.html         
├── signup.html          
├── signin.html          
├── orders.html          
├── welcome.html                
├── css/
│   ├── style.css            
│   ├── explore.css          
│   ├── signup.css           
│   ├── signin.css           
│   ├── cart.css             
│   └── welcome.css          
├── images/
│   ├── Rectangle 1.png       
│   ├── Desktop - 4.png      
│   ├── explorehero.png      
│   ├── Welcome.png          
│   ├── image 1.png
│   └── Search_Magnifying_Glass.svg 
```

### Key Files Explained

| `signup.css` / `signin.css` | Authentication flows - two-column layout with image overlay and form |
| `style.css` | Global nav, hero banner, product cards, and footer styling |
| `explore.css` | Menu grid, category filters, and product listing with ratings |
| `cart.css` | Shopping cart interface and checkout flow |

## Design Interpretation

### Color Palette
The design uses a warm, inviting color system reflecting Nigerian culinary culture:

```css
--primary-orange: #ff7a18;
--soft-orange: #ffb066;
--light-orange: #ffe1c4;
--dark-orange: #c95400;
--primary-pink: #ff4f9a;
--soft-pink: #ff9ac7;
--light-pink: #ffe1ee;
--dark-pink: #b0005a;
--primary-blue: #1e88e5;
--soft-blue: #64b5f6;
--light-blue: #e3f2fd;
--dark-blue: #0d47a1;
--pure-white: #ffffff;
--soft-gray: #f3f4f6;
--charcoal-black: #1f2937;
--dark-gray: #4b5563;
--muted-gray: #9ca3af;
--brown: #62422E;
```

### Layout Approach

#### Authentication Pages (Sign-up / Sign-in)
- **Two-column layout**: 50/50 split with image on left, form on right
- **Image section**: Hero photo with semi-transparent orange overlay (`rgba(255, 122, 24, 0.75)`)
- **Form section**: Centered input fields with icon prefixes (envelope for email, lock for password)
- **Icon integration**: FontAwesome for standard icons

#### Homepage
- **Navigation bar**: Fixed/sticky header with logo and menu links
- **Hero banner**: Full-width with search functionality and CTA button
- **Product grid**: Showcase popular menu categories and featured items
- **Footer**: Multi-column layout with links, contact info, and social links

#### Menu/Explore Page
- **Category navigation**: Horizontal scrollable or tabbed menu categories
- **Product cards**: Consistent grid layout with image, title, rating, and price
- **Responsive grid**: Adjusts from 4 columns (desktop) → 2 columns (tablet) → 1 column (mobile)

#### Shopping Cart
- **Cart items**: List view with quantity controls and remove options
- **Order summary**: Sticky sidebar with subtotal, delivery fee, and total
- **Checkout button**: Prominent call-to-action at bottom of cart

### Design Decisions & Assumptions

1. **Facebook Button** (Design Decision): Button was written as "Continue with Apple" but had facebook icon. This was corrected to "Continue with Facebook" to match the icon on sign in and sign up pages.

2. **Footer Integration on Mobile view** (Addition): Full-featured footer with 4-column grid layout, contact information, quick links, and social media links added to sign-up/sign-in pages. Original mockups showed only the form section; footer was added for consistency across all pages.

3. **Hover States on Buttons** (Enhancement): Buttons now have hover states with slightly darker background colors.

4. **Icon on Welcome Page** (Enhancement): The icon used to represent "Support Local Business" on the welcome page was updated to match the statement.

## Limitations & Improvements

### Current Limitations
1. **JavaScript Interactivity**: JavaScript implementation for interactive elements
2. **Form Backend**: Authentication endpoints not yet connected - forms are static HTML
3. **Product Data**: Menu items and pricing are hardcoded - no dynamic content management
4. **Mobile Navigation**: Hamburger menu button present but toggle functionality not implemented
5. **Search Functionality**: Search bar visible but not wired to backend API
6. **Cart Persistence**: No local storage or session management for cart data

### Recommended Improvements for Next Phase

#### High Priority
- [ ] Implement JavaScript for password visibility toggle on auth pages
- [ ] Add form validation (email format, password strength, required fields)
- [ ] Create reusable JavaScript modules for mobile menu toggle and search
- [ ] Connect authentication forms to backend API (signup, signin, OAuth)
- [ ] Implement shopping cart functionality with localStorage persistence

#### Medium Priority
- [ ] Add JavaScript animations/transitions for smoother UX
- [ ] Create dynamic menu rendering from JSON data structure
- [ ] Implement image lazy-loading for performance optimization
- [ ] Add loading states and error handling on forms
- [ ] Create responsive image handling with srcset for different device sizes

#### Low Priority (Polish & Analytics)
- [ ] Implement accessibility testing and 508 compliance
- [ ] Add Google Analytics and event tracking
- [ ] Create CSS animation library for page transitions
- [ ] Optimize critical rendering path for faster load times
- [ ] Add progressive web app (PWA) capabilities for offline functionality

## Development Notes for the Next Developer

### Getting Started
1. All CSS uses custom properties (variables) defined in `:root` - these centralize color and spacing decisions
2. Each page has its own stylesheet
3. Font imports via Google Fonts and Font Awesome CDN are already linked in each HTML file

### Architecture Recommendations
- **Component-based CSS**: Break signup/signin forms into reusable button and input component styles
- **State Management**: Plan JavaScript module structure for form state, cart, and user authentication
- **API Integration Layer**: Create a `js/api.js` module for all backend communication

### Testing Checklist
- [ ] Cross-browser testing (Chrome, Firefox, Safari, Edge)
- [ ] Mobile viewport testing at common breakpoints
- [ ] Form validation and accessibility testing
- [ ] Image optimization and lazy-loading verification
- [ ] Performance audit with Lighthouse

### Live URL
https://friendly-bienenstitch-c5e310.netlify.app/

---
**Last Updated**: February 2026  
**Current Status**: Frontend structure complete