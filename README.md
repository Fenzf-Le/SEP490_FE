# SEP490_FE - Manga Mystery Box collect and Trade App

- Abbreviation: MMB
A React + Vite web application for a collectible trading platform featuring auctions, product management, mystery boxes, real-time communication, and adminitration dashboard. Built for the Capstone project.

## Technologies

- **Framework:** React 18
- **Build Tool:** Vite
- **Language:** JavaScript (JSX)
- **State Management:** Redux Toolkit
- **HTTP Client:** Axios
- **Real-time Communication:** Socket.io
- **UI Components:** Custom components
- **Database/Auth:** Supabase
- **Payment Gateway:** PayOS
- **Styling:** CSS (with CSS Modules) & Tailwind CSS

## Requirements

- Node.js (>= 18 recommended)
- npm or yarn
- Git

## Setup & Run

### Installation

1. Clone the repository
   ```bash
   git clone <repository-url>
   cd SEP490_FE
   ```

2. Install dependencies
   ```bash
   npm install
   # or
   yarn install
   ```

3. Environment Configuration
   Create a `.env` file in the project root and configure

### Development

Start the development server with hot module replacement (HMR):
```bash
npm run dev
# or
yarn dev
```

The application will be available at `http://localhost:5173` (or the port specified by Vite).

### Production Build

Build for production:
```bash
npm run build
# or
yarn build
```

Preview the production build locally:
```bash
npm run preview
# or
yarn preview
```

## Project Structure

```text
/src
├── assets/              # Images, icons, SVGs
│   ├── carousel/
│   ├── homeGallery/
│   ├── Icon_fill/
│   ├── Icon_line/
│   ├── logoSVG/
│   ├── pageBG/
│   └── others/
├── components/          # Reusable UI and page components
│   ├── adminPages/      # Admin dashboard and management pages
│   ├── moderatorPages/  # Moderator dashboard and pages
│   ├── pages/           # User-facing pages
│   ├── libs/            # Reusable library components
│   └── instants/        # Animated/instant components
├── config/              # Configuration files
│   ├── axios.js         # API client configuration
│   ├── socket.js        # Socket.io configuration
│   └── supabase.js      # Supabase configuration
├── context/             # React Context for global state
│   ├── ChatContext.jsx
│   └── ThemeContext.jsx
├── hooks/               # Custom React hooks
├── redux/               # Redux store and slices
│   ├── store.js
│   ├── rootReducer.js
│   └── features/
├── router/              # Routing configuration
│   ├── routerConfig.jsx
│   └── Pathname.js
├── services/            # API service modules
│   ├── api.auth.js
│   ├── api.auction.js
│   ├── api.product.js
│   ├── api.user.js
│   ├── api.admin.js
│   └── ... (other services)
├── utils/               # Utility functions
│   ├── currency.js
│   └── upload.js
├── App.jsx
├── main.jsx
└── index.css
```

## Features & Roles

<details>
<summary><strong>👤 Collector Features</strong></summary>

- **Browse & Search:** Explore products with search and filtering
- **Product Details:** View detailed product information
- **Shopping Cart:** Add/remove items and checkout
- **Exchange:** Request for trading collectibles with other collectors
- **Auctions:** Participate in live auctions with real-time updates
- **Mystery Boxes:** Purchase mystery boxes for random collectibles
- **Collections:** Manage personal collection of collectibles
- **Chat:** Real-time messaging with other collectors
- **Wishlist/Favorites:** Save favorite items
- **User Profile:** View and edit profile information
- **Activities History:** Track past purchases and transactions

</details>

<details>
<summary><strong>🛠 Admin Features</strong></summary>

- **Dashboard:** Overview of platform statistics
- **User Management:** Manage user accounts and roles
- **Product Management:** Add, edit, and manage products
- **Auction Management:** Create and manage auctions
- **Auction Results:** View auction outcomes
- **Revenue Reports:** Track platform revenue
- **Report Management:** Handle collector reports and disputes
- **System Moderation:** Content and user moderation tools

</details>

<details>
<summary><strong>🛡 Moderator Features</strong></summary>

- **Auction Moderation:** Review and moderate auctions
- **Product Approval:** Approve or reject products
- **Collection Review:** Manage collections
- **Mystery Box Management:** Oversee mystery box distributions
- **Report Resolution:** Address collector reports
- **Withdraw Requests:** Process withdrawal requests
- **User Reports:** Track and manage reported content

</details>


## Key Components

- **Navigation:** Main navigation and dropdown menus
- **Carousel:** Product and content carousels
- **Modals:** Confirmation, login, OTP, messaging modals
- **Forms:** Login, register, product selling forms
- **Cards:** Product and collection card components
- **Comments:** User comment sections
- **Sidebar:** Admin and moderator sidebars

## API Integration

The application communicates with a backend API for:
- Authentication and user management
- Product catalog
- Auction management
- Orders and transactions
- Chat messaging
- File uploads
- Payment processing via PayOS

See individual service files in `/src/services/` for API endpoint details.

## State Management

- **Redux Toolkit:** For global application state
- **React Context:** For theme and chat state
- **AsyncStorage:** For local client-side data persistence (via Supabase)

## Notes for Development

- Ensure all environment variables are properly configured before running
- Socket.io is used for real-time features (auctions, chat, notifications)
- PayOS integration handles payment processing
- Supabase provides authentication and database services
- ESLint is configured for code quality

## Deployment

The project is configured for deployment on Vercel (see `vercel.json` for configuration). To deploy:

1. Push your code to a Git repository (GitHub, GitLab, etc.)
2. Import the repository to Vercel
3. Configure environment variables in Vercel dashboard
4. Vercel will automatically build and deploy on each push to the main branch

## License

This project is proprietary and confidential. All rights reserved by MMB-SEP490 Project Team.
