# Bridgeway — Landing Page

A responsive landing page for Bridgeway, a payment solutions platform. Built with Vue 3, TypeScript, Vite, and Tailwind CSS, with a focus on visual accuracy, responsive layouts, and subtle interactions.

## Tech Stack

- **Vue 3** — Component-based UI development using the Composition API and `<script setup>`.
- **TypeScript** — Type safety and clearer component interfaces.
- **Vite** — Development server and production build tooling.
- **Tailwind CSS** — Responsive styling and utility-first CSS.
- **ESLint & Prettier** — Code quality and consistent formatting.

## Getting Started

### Prerequisites

- Node.js (LTS recommended)
- npm

### Installation

Clone the repository and install the dependencies:

```bash
git clone <your-repository-url>
cd <project-folder>
npm install
```

### Run Locally

Start the development server:

```bash
npm run dev
```

Open the local URL displayed in your terminal.

### Production Build

Build the project for production:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## Project Structure

The project uses a lightweight, component-based structure that keeps the code organized without introducing unnecessary complexity for a single-page landing page.

```text
src/
├── assets/
│   ├── images/
│   └── fonts/
├── components/
│   ├── layout/
│   │   ├── MainNavbar.vue
│   │   └── MainFooter.vue
│   └── ui/
│       └── BaseButton.vue
├── pages/
│   └── HomeView.vue
│   └── components/
│       └──  AppSection
├── App.vue
├── main.ts
└── style.css
```

*Note: The tree above illustrates the intended organization. Adjust file and folder names to match the final repository.*

### Why This Structure?

- **`components/layout/`** contains shared structural elements such as the navbar and footer.
- **`components/ui/`** contains reusable interface elements, such as the base button, that can be used across different sections.
- **`pages/`** composes the page from its sections and components.
- **`assets/`** centralizes images, icons, and fonts.

This approach makes components easier to locate, maintain, and reuse while keeping the architecture appropriate for the scope of the project.

## Implementation Highlights

- Reusable Vue components with typed props and events.
- Data-driven rendering for repeated navigation links, feature cards, and social links.
- Responsive layouts using Tailwind CSS breakpoints.
- Subtle hover transitions for interactive elements.
- Semantic HTML and descriptive alternative text where appropriate.
- Locally managed visual assets and fonts.

## Hardest Part & Solution

**Maintaining visual consistency across different screen sizes** was one of the main challenges, particularly when positioning decorative artwork and aligning the hero content with the surrounding imagery.

I addressed this by using relative positioning for section containers, absolute positioning only where the design required layered elements, and Flexbox or Grid for the main layout. I also used responsive Tailwind utilities to adjust spacing, sizing, and alignment at larger breakpoints.

The goal was to preserve the intended visual composition without relying on excessive fixed offsets or duplicating components for different screen sizes.

## What I Would Improve With More Time

- Test and refine the layout across a wider range of viewport sizes and browsers.
- Improve keyboard navigation, focus states, and accessibility checks.
- Review image dimensions and loading behavior to improve performance.
- Add more detailed interaction states where appropriate.
- Extract additional shared patterns only where they provide meaningful reuse.
- Add automated tests for important component behavior if the project grows.

## Differences From the Design

The implementation aims to follow the supplied design as closely as possible.

- **Responsive behavior:** Some layouts and spacing may adapt at different viewport sizes to preserve readability and usability.
- **Mobile layout:** Elements may be reordered or decorative assets hidden on smaller screens where necessary to maintain a usable layout.

Any remaining differences should be documented here explicitly after the final comparison with the supplied design.

## License

Created as part of a frontend development assessment. All supplied design assets are used for assessment purposes.