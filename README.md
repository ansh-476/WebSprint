# ADAPTILEARN — Multiverse Learning HQ

ADAPTILEARN is a single-page, browser-based learning dashboard prototype built with **HTML, CSS, and vanilla JavaScript**. It presents an interactive "Multiverse Learning HQ" where users can browse courses, track learning activity, practice interviews, view analytics, manage a profile, and personalize settings.

## ✨ Features

- **Dashboard**
  - Learning velocity chart
  - Progress statistics
  - Current mastery goal
  - Personalized course recommendations

- **Courses**
  - Featured course cards
  - Course categories and filters
  - Course search
  - Course mission launch interaction

- **My Learning**
  - Enrolled/completed mission overview
  - Telemetry statistics
  - Recent activity section

- **Revision**
  - Spaced-repetition themed revision area
  - Revision queue interface

- **Projects**
  - Beginner project mission recommendations
  - Project technology stacks
  - Mission briefing modal

- **Interview Prep**
  - AI mock-interview styled interface
  - Answer submission
  - Evaluation modal

- **Analytics**
  - Daily learning-time visualization
  - Accuracy trend chart
  - Learning and mastery metrics

- **Profile**
  - User profile and multiverse identity
  - Learning statistics
  - Achievement badges
  - Activity grid

- **Settings**
  - Light/dark mode toggle
  - Preference-saving interaction

- **Authentication UI**
  - Login screen
  - Email/username and access-code fields
  - Google/GitHub connection buttons

- **Responsive Design**
  - Desktop sidebar navigation
  - Tablet layout adjustments
  - Mobile navigation behavior
  - Responsive grids and authentication layout

## 🛠️ Technologies Used

- **HTML5**
- **CSS3**
- **Vanilla JavaScript**
- **Google Fonts — Archivo**
- **SVG** for the analytics accuracy chart
- Local image assets

No frontend framework or build system is required.

## 📁 Project Structure

```text
project/
├── index.html
├── README.md
├── assets/
│   ├── logo.jpg
│   ├── spider.jpg
│   ├── course1.jpg
│   ├── course2.jpg
│   ├── course3.jpg
│   ├── course4.jpg
│   ├── course5.jpg
│   └── course6.jpg
└── miles_standing.webp
```

> Keep the referenced image files in the same relative locations used by `index.html`, otherwise some visual elements will not load.

## 🚀 Getting Started

### 1. Download or clone the project

Place `index.html` and the required `assets/` files inside the same project directory.

### 2. Open the website

Because this project is a static HTML application, it can be opened directly in a browser:

```text
index.html
```

Alternatively, run it through a local development server.

For example, with VS Code you can use the **Live Server** extension.

## 🧭 Navigation

The application uses URL hash routing rather than a backend router.

Available routes include:

```text
#/dashboard
#/courses
#/learning
#/revision
#/projects
#/interview
#/analytics
#/profile
#/settings
#/login
```

The JavaScript reads the current hash and renders the corresponding page.

## 🎨 Design System

The interface uses a bold comic/neobrutalist-inspired visual style.

Main design characteristics:

- Thick black borders
- Offset hard shadows
- Rounded cards
- Bright accent colors
- Bold typography
- Comic/multiverse-inspired terminology
- Responsive grid layouts
- Dotted page background

Primary CSS theme colors include:

```text
Red:    #ff0038
Cyan:   #00d9ee
Yellow: #ffe600
Pink:   #ff0084
Ink:    #17171a
```

The main font is **Archivo**.

## ⚙️ How the JavaScript Works

The application keeps its UI state in a small JavaScript object:

```js
const state = {
  route: "dashboard",
  dark: false,
  menu: false
};
```

The `render()` function determines the current route and injects the corresponding page into the `#root` element.

Navigation is handled with:

```js
window.addEventListener("hashchange", render);
```

This allows the website to behave like a lightweight single-page application without React, Vue, Angular, or another framework.

## 🔍 Course Search & Filtering

The course database is stored in a JavaScript array containing course images, categories, titles, authors, views, and likes.

Users can:

- Search by course title
- Search by category
- Search by author
- Filter courses by category
- Launch a course mission

The current implementation performs filtering entirely in the browser.

## 🌓 Dark Mode

The settings page and top navigation provide a dark-mode toggle.

The current implementation applies a visual inversion using:

```js
document.body.style.filter = "invert(.9) hue-rotate(180deg)";
```

This is a prototype implementation rather than a full separate dark-theme color system.

## 💬 Interactive Components

The website includes several reusable interaction functions:

- `toggleMenu()` — opens/closes the mobile sidebar
- `toast()` — displays temporary notifications
- `openModal()` — opens mission/evaluation dialogs
- `closeModal()` — closes dialogs
- `startMission()` — starts a course mission interaction
- `doLogin()` — handles the prototype login action
- `sendAnswer()` — handles interview answer submission
- `toggleTheme()` — switches the visual theme
- `filterCourses()` — filters course cards
- `searchCourses()` — searches course cards

## 📊 Current Prototype Limitations

This is currently a **frontend prototype**. It does not include a real backend or persistent database.

For example:

- Login does not authenticate against a server.
- Course progress is not persisted.
- Interview evaluation is simulated.
- Google/GitHub buttons are UI interactions only.
- Analytics use static/demo values.
- Learning history is not stored in a database.
- Settings are not persisted between page reloads.
- Course missions display prototype interactions rather than full course playback.

## 🔮 Possible Future Improvements

A production version could add:

1. User authentication with Firebase/Auth0/custom backend.
2. Database storage for profiles and learning progress.
3. Real course/video integration.
4. AI-powered interview evaluation.
5. AI-generated personalized learning paths.
6. Persistent revision decks using spaced repetition.
7. Real-time analytics.
8. Course progress tracking.
9. Backend APIs.
10. User-specific recommendations.
11. Achievement and badge progression.
12. Cloud deployment and CI/CD.

## 📄 License

This project is provided as a frontend prototype. Add your preferred license here if you plan to distribute the project publicly.

## 👨‍💻 Project

**ADAPTILEARN — Multiverse Learning HQ**

A futuristic adaptive-learning dashboard concept combining education, gamification, analytics, projects, revision, and interview preparation into one interface.
