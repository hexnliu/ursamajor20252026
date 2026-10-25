# Ursa Major 9180 Robotics Website

The website for Ursa Major 9180, the robotics team at Grandview Heights Secondary School in Surrey, British Columbia. The team competes in FIRST Robotics Competition (FRC) and FIRST LEGO League (FLL).

## Features

- Home page introducing the team and its Saturday LEGO Robotics Camps.
- Pages for About Us, sponsors, team members and credits, LEGO workshops, and FIRST.
- Responsive navigation with desktop links and a mobile menu.
- Sponsor dialog with a downloadable sponsorship packet and an embedded sponsorship form.
- Contact action that opens an email draft addressed to `ghs.ursa.major@gmail.com`.

## Navigation

The navigation component is `src/components/Navbar.jsx`. It uses React Router links for internal pages and highlights the active page based on the current path.

| Label | Destination |
| --- | --- |
| Home Page | `/` |
| About Us | `/about` |
| About FIRST® | Opens [firstinspires.org](https://www.firstinspires.org/) in a new tab |
| Sponsors | `/sponsors` |
| Team Members & Credits | `/team-members` |
| LEGO Workshops | `/lego-workshops` |

The app also defines `/first` and `/dependencies` routes, but they are not linked in the navbar. The Search control is currently visual only and does not perform a search.

On smaller screens, the hamburger button opens a mobile menu. Selecting an internal page closes the menu; the backdrop also closes it.

### Sponsor Us

Opens a dialog with the sponsorship packet at `src/images/SponsorshipPackage2526.pdf` and an embedded Google Form. The dialog can be closed with its close button or by clicking the overlay.

### Contact Us

Creates a pre-filled email draft with a suggested subject and message body. The component then displays a dialog explaining what to check if the default email application does not open.

## Technology

- React 18
- React Router
- Lucide React icons
- Create React App (`react-scripts`)

## Getting started

From the `my-react-app` directory, install dependencies and start the development server:

```bash
npm ci
npm start
```

The app opens at [http://localhost:3000](http://localhost:3000).

## Available scripts

| Command | Description |
| --- | --- |
| `npm start` | Starts the development server. |
| `npm test` | Runs the test suite in watch mode. |
| `npm run build` | Creates an optimized production build in `build/`. |
| `npm run deploy` | Builds the app and deploys the `build/` directory with `gh-pages`. |
| `npm run eject` | Ejects the Create React App configuration. This is a one-way operation. |

## Project structure

```text
src/
  App.js                 Main app and route definitions
  components/
    Navbar.jsx           Site navigation and sponsor/contact dialogs
    Footer.jsx           Site footer
    Sponsors.jsx         Sponsors page
    aboutus.jsx          About page
    legoWorkshops.jsx    LEGO workshops page
    teamMembers.jsx      Team members and credits page
  images/                Site images, logo, and sponsorship packet
```

The app uses `BrowserRouter` in `src/index.js`; keep it in place for the navbar's internal links and route-aware active state to work.
