# Naseem-e-Sehar Library

## Overview

Naseem-e-Sehar Library is a beautiful digital book collection platform that allows you to publish and share your digital books stored on Google Drive. Visitors can browse your library and read any book by clicking "Read Now", which opens the book's PDF directly in Google Drive.

## How to Use

### Adding Your Books

1. Click the **"Add My Book"** button on the homepage
2. Fill in the book details:
   - **Title**: Enter the name of your book
   - **Google Drive PDF Link**: Paste your book's Google Drive sharing link
   - **Thumbnail URL** (optional): Add a cover image URL for your book
3. Click "Add Book" to save

### Getting Google Drive Links

1. Upload your PDF to Google Drive
2. Right-click the file and select "Get link" 
3. Make sure sharing is set to "Anyone with the link can view"
4. Copy and paste the link into the Add Book form

### Managing Your Library

- Books appear automatically on the homepage after adding
- Use the search bar to filter books by title
- The Library page offers grid and list view options
- Sample books are included for demonstration - you can replace them with your own

## Recent Changes

- Initial release with complete library functionality
- Home, Library, and Contact pages
- Add Book modal for easy book management
- Search functionality
- Light/Dark theme toggle
- Responsive design for all devices

## Technical Architecture

### Frontend
- React 18 with TypeScript
- Tailwind CSS with custom warm library theme
- Shadcn/UI components
- Playfair Display font for elegant headings
- Inter font for readable body text

### Backend
- Express.js server
- In-memory storage (books persist until server restart)
- RESTful API at `/api/books`

### API Endpoints
- GET `/api/books` - Get all books
- POST `/api/books` - Add a new book
- DELETE `/api/books/:id` - Remove a book

### Key Files
- `client/src/pages/home.tsx` - Homepage with hero and book grid
- `client/src/pages/library.tsx` - Library browser page
- `client/src/pages/contact.tsx` - Contact form page
- `client/src/components/add-book-modal.tsx` - Add book form
- `client/src/components/book-card.tsx` - Book display card
- `server/routes.ts` - API routes
- `server/storage.ts` - Data storage

## User Preferences

- Clean, modern design with warm library aesthetics
- Simple admin interface for adding books
- Google Drive integration for PDF hosting
- Responsive layout for all devices
