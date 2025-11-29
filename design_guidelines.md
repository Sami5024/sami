# Design Guidelines: Naseem-e-Sehar Library

## Design Approach

**Reference-Based Design** inspired by premium content platforms (Apple Books, Medium, Google Books) combined with the organizational clarity of Notion. This creates a sophisticated digital library that feels premium, inviting, and easy to navigate.

## Typography

**Primary Font:** Playfair Display (Google Fonts) - elegant serif for the library title and headings
**Secondary Font:** Inter (Google Fonts) - clean sans-serif for body text, buttons, and UI elements

**Hierarchy:**
- Library Title: 4xl to 6xl, Playfair Display, font-weight 600
- Section Headings: 2xl to 3xl, Playfair Display, font-weight 600
- Book Titles: xl, Inter, font-weight 600
- Body Text: base, Inter, font-weight 400
- Buttons: base, Inter, font-weight 500, uppercase tracking

## Layout System

**Spacing Units:** Tailwind units of 4, 6, 8, 12, 16, 24
- Container max-width: max-w-7xl
- Section padding: py-16 md:py-24
- Card spacing: gap-6 md:gap-8
- Component padding: p-6 md:p-8

## Component Library

### Navigation Bar
- Fixed top position with subtle backdrop blur
- Logo/title on left, navigation links centered, admin button on right
- Height: h-20, horizontal padding px-6 md:px-12
- Links with subtle underline animation on hover

### Hero Section
- Center-aligned with library title prominently displayed
- Subtitle describing the library's purpose
- Search bar directly below (max-w-2xl, rounded-full, with search icon)
- Minimal height: 60vh with elegant spacing
- "Add My Book" admin button positioned top-right corner (fixed or in nav)

### Book Grid
- Responsive grid: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4
- Gap: gap-6 md:gap-8
- Cards with subtle shadow and rounded corners (rounded-xl)

### Book Cards
- Aspect ratio 3:4 for thumbnail area
- Thumbnail fills top portion, gradient overlay if no image
- Title below thumbnail: 2 lines max with ellipsis
- "Read Now" button at bottom: full-width, rounded-lg
- Card hover: subtle lift effect (transform translateY)
- Padding: p-6

### Admin Interface Modal
- Centered overlay with backdrop blur
- Form container: max-w-2xl, rounded-2xl, p-8
- Input fields: w-full, rounded-lg, spacing mb-6
- Labels: text-sm, font-medium, mb-2
- Submit button: prominent, full-width or centered

### Search Bar
- Rounded-full design with generous padding (px-6 py-4)
- Search icon on left, clear button on right
- Sticky behavior on scroll (optional implementation)
- Max-width: max-w-2xl for optimal usability

### Contact Page
- Two-column layout: md:grid-cols-2
- Left: Contact form with name, email, message fields
- Right: Library information, address, social links
- Form inputs: rounded-lg, consistent spacing mb-4

## Animations

**Minimal, purposeful animations only:**
- Card hover: subtle scale (1.02) and shadow increase
- Button hover: slight brightness change
- Page transitions: gentle fade-in
- Modal: scale and fade entrance
- Navigation: smooth scroll behavior

## Images

**Hero Section:** 
Large background image of elegant bookshelves, warm library interior, or abstract book-related imagery. Image should be subtle, slightly desaturated to allow text overlay readability. Position: center, cover. Height: 60vh minimum.

**Book Thumbnails:**
User-provided optional thumbnail URLs. If not provided, display elegant gradient placeholder with book icon or first letter of title in large typography.

**Fallback Strategy:**
Use geometric gradients or single-color backgrounds for missing thumbnails to maintain visual consistency.

## Page Structure

**Homepage:**
1. Navigation bar
2. Hero section with title + search
3. Book grid (all 35 books displayed)
4. Footer with quick links

**Library Page:**
Same as homepage with enhanced filtering/sorting options

**Contact Page:**
Two-column form layout with library information

## Responsive Behavior

**Mobile (< 768px):**
- Single column book grid
- Stacked navigation (hamburger menu)
- Full-width search bar
- Reduced spacing (py-12 instead of py-24)

**Tablet (768px - 1024px):**
- 2-column book grid
- Horizontal navigation
- Balanced spacing

**Desktop (> 1024px):**
- 3-4 column book grid
- Full navigation with all options visible
- Maximum spacing and breathing room

## Critical Implementation Notes

- All "Read Now" buttons open Google Drive links in new tab (target="_blank" rel="noopener noreferrer")
- Search filters books client-side by title match
- Admin modal appears on "Add My Book" click with form fields: Title (required), Google Drive Link (required), Thumbnail URL (optional)
- Books stored and displayed dynamically
- Maintain elegant, library-appropriate aesthetic throughout - avoid overly playful or casual design elements