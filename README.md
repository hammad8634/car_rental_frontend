# Milele Car Rental Frontend

[![React](https://img.shields.io/badge/React-18-20232a?logo=react)](https://react.dev/)
[![Repository](https://img.shields.io/badge/GitHub-Public-181717?logo=github)](https://github.com/hammad8634/car_rental_frontend)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](#contributing)

A production-oriented React frontend for a car-rental platform. The application supports vehicle discovery, booking and document-verification workflows, customer accounts, location features, multilingual content, analytics, and SEO-focused pages.

**Repository:** [github.com/hammad8634/car_rental_frontend](https://github.com/hammad8634/car_rental_frontend)

## Project overview

Milele Car Rental Frontend is designed to cover the customer journey from browsing available vehicles to submitting a booking and managing an account.

The project has grown through more than 400 commits and is under active development. The current focus is improving maintainability, automated testing, accessibility, performance, documentation, and the reliability of the booking experience.

## Main features

- Browse and explore available rental vehicles
- Vehicle details, pagination, and fleet content
- Multi-step booking and verification workflow
- Customer authentication and protected routes
- Password reset and password update flows
- Customer profile and booking-management pages
- Google Maps and Leaflet-based location features
- Internationalisation using i18next
- Contact, about, terms, and informational pages
- Rental and travel-related blog content
- Expense calculator
- Google Analytics integration
- SEO metadata and sitemap generation
- Responsive interface built with reusable React components
- Automated build and cPanel deployment through GitHub Actions

## Technology stack

| Area | Technology |
|---|---|
| Frontend | React 18, Create React App |
| Routing | React Router 6 |
| API communication | Axios |
| UI | Material UI, Ant Design, Bootstrap, MDB UI Kit |
| Maps | Google Maps API, Leaflet, React Leaflet |
| Localisation | i18next, react-i18next |
| Forms and selection | React Select, date and phone-input libraries |
| Notifications | React Hot Toast, React Toastify |
| Analytics and SEO | React GA, React Helmet, sitemap |
| Testing | Jest, React Testing Library |
| Deployment | GitHub Actions, cPanel, FTP deployment |

## Application routes

Examples of routes currently implemented in the application include:

| Route | Purpose |
|---|---|
| `/` | Home page |
| `/vehicles` | Vehicle catalogue |
| `/booking-page/:step` | Multi-step booking workflow |
| `/my-profile/:id` | Protected customer profile |
| `/my-bookings/:id` | Protected customer bookings |
| `/reset-password/:token` | Password reset |
| `/update-password` | Protected password update |
| `/map` | Map page |
| `/expense-calculator` | Expense calculator |
| `/about-us` | About page |
| `/contact-us` | Contact page |
| `/terms-and-conditions` | Terms and conditions |
| `/rent-a-car-in-sharjah` | Location-focused content page |

## Getting started

### Prerequisites

Install the following before running the project:

- Node.js
- npm
- Access to the required backend and third-party services

### Installation

Clone the repository:

```bash
git clone https://github.com/hammad8634/car_rental_frontend.git
cd car_rental_frontend
```

Install the dependencies:

```bash
npm install
```

Create a local environment file:

```bash
cp .env.example .env
```

Add your own development values to `.env`, then start the application:

```bash
npm start
```

The development server will normally be available at:

```text
http://localhost:3000
```

## Environment variables

Create a `.env.example` file containing variable names only:

```env
REACT_APP_GOOGLE_MAPS_KEY=
REACT_APP_INSTAGRAM_TOKEN_KEY=
REACT_APP_SPEED_API_BEARER_TOKEN=
REACT_APP_MILELE_API_URL=
REACT_APP_OPENCAGE_KEY=
```

Never commit real credentials or access tokens.

Values prefixed with `REACT_APP_` are included in the browser build and must not be treated as private secrets. Sensitive service credentials should be stored and used by a secure backend rather than directly by the React client.

## Available scripts

### Start the development server

```bash
npm start
```

### Run tests

```bash
npm test
```

### Create a production build

```bash
npm run build
```

The optimised application is generated in the `build/` directory.

### Generate the sitemap

```bash
npm run generate-sitemap
```

### Eject Create React App

```bash
npm run eject
```

Ejecting is irreversible and is generally unnecessary for normal development.

## Project structure

```text
car_rental_frontend/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── public/
├── src/
│   ├── components/
│   │   ├── GoogleMap/
│   │   ├── Pages/
│   │   │   ├── Blog/
│   │   │   ├── OtherPages/
│   │   │   ├── Utils/
│   │   │   ├── homePage/
│   │   │   ├── multipleStepsForm/
│   │   │   └── vehicle/
│   │   ├── PrivateComponents/
│   │   ├── authentication/
│   │   └── customerDashboard/
│   ├── App.js
│   ├── Map.jsx
│   ├── i18n.js
│   └── index.js
├── generateSitemap.js
├── package.json
└── README.md
```

## Deployment

The repository contains a GitHub Actions workflow that builds the application after changes are pushed to the `main` branch and deploys the contents of `build/` to cPanel through FTP.

Deployment credentials and environment values must be stored in GitHub Actions Secrets, not in the repository.

Expected deployment secrets include:

```text
FTP_SERVER
FTP_USERNAME
FTP_PASSWORD
REACT_APP_GOOGLE_MAPS_KEY
REACT_APP_INSTAGRAM_TOKEN_KEY
REACT_APP_SPEED_API_BEARER_TOKEN
REACT_APP_MILELE_API_URL
REACT_APP_OPENCAGE_KEY
```

## Development roadmap

Planned improvements include:

- Expand unit and integration test coverage
- Add automated linting, testing, and security checks to CI
- Improve accessibility and keyboard navigation
- Improve loading, empty, and error states
- Refactor large components into smaller reusable modules
- Centralise API communication and error handling
- Improve responsive behaviour across devices
- Optimise images and application performance
- Improve setup, architecture, and contribution documentation
- Add additional localisation coverage

## Contributing

Contributions, bug reports, and improvement suggestions are welcome.

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. Make and test your changes.
4. Commit with a clear message:

   ```bash
   git commit -m "Add: describe your change"
   ```

5. Push the branch:

   ```bash
   git push origin feature/your-feature-name
   ```

6. Open a pull request describing the problem and your solution.

Please avoid including credentials, personal information, or production data in issues and pull requests.

## Maintainer

**Hammad Mukhtar**

- GitHub: [@hammad8634](https://github.com/hammad8634)
- Project: [car_rental_frontend](https://github.com/hammad8634/car_rental_frontend)

## Licence

A licence has not yet been added to this repository. Before reusing or distributing the project, review the repository permissions. The maintainer should add an appropriate open-source licence if public reuse and contribution are intended.

## Acknowledgements

This project uses React and a collection of open-source libraries for routing, interface components, maps, localisation, testing, analytics, and deployment. Thanks to the maintainers and contributors of those projects.
