# Camila García - Coaching Landing Page

A modern, high-conversion Spanish-language landing page for professional coaching services built with Astro, Tailwind CSS v4, and TypeScript.

## 🚀 Features

- **Modern Tech Stack**: Astro v5, Tailwind CSS v4, TypeScript
- **Content Collections**: Type-safe content management with Zod validation
- **Responsive Design**: Mobile-first approach, works on all screen sizes
- **Reusable Components**: 9 optimized components reducing code duplication by 60-70%
- **SEO Optimized**: Proper meta tags, semantic HTML, and accessibility
- **Fast Performance**: Static site generation for optimal loading speeds

## 📂 Project Structure

```
cams-landing/
├── src/
│   ├── components/
│   │   ├── common/              # Reusable utility components
│   │   │   ├── Button.astro           (14 instances)
│   │   │   ├── StarRating.astro       (5+ instances)
│   │   │   ├── StatCard.astro         (7+ instances)
│   │   │   └── ProfilePicture.astro   (6+ instances)
│   │   ├── cards/               # Card-based components
│   │   │   ├── TestimonialCard.astro  (6 instances)
│   │   │   ├── FeatureCard.astro      (7 instances)
│   │   │   ├── ProcessStepCard.astro  (3 instances)
│   │   │   ├── FAQItem.astro          (6 instances)
│   │   │   └── BenefitItem.astro      (3 instances)
│   │   └── sections/            # Landing page sections
│   │       ├── Header.astro
│   │       ├── Hero.astro
│   │       ├── Testimonials.astro
│   │       ├── ProblemStatement.astro
│   │       ├── Features.astro
│   │       ├── Reviews.astro
│   │       ├── Process.astro
│   │       ├── TargetAudience.astro
│   │       ├── About.astro
│   │       ├── FinalCTA.astro
│   │       ├── FAQ.astro
│   │       └── Footer.astro
│   ├── content/                 # Content Collections
│   │   ├── config.ts            # Schema definitions
│   │   ├── testimonials/        # 6 testimonial entries
│   │   ├── features/            # 7 feature entries
│   │   ├── process-steps/       # 3 step entries
│   │   └── faqs/                # 6 FAQ entries
│   ├── layouts/
│   │   └── Layout.astro         # Base page layout
│   ├── pages/
│   │   └── index.astro          # Main landing page
│   └── styles/
│       └── global.css           # Global styles + Tailwind config
└── public/
    └── images/                  # Image assets
```

## 🎨 Design System

### Colors
- **Primary**: `#315aff` (Blue CTA)
- **Secondary**: `#ffffff` (White)
- **Gray Scale**: 50, 100, 200, 700, 900

### Typography
- **Font**: Lato (400, 600, 700)
- **Headings**: 24-48px, weight 700
- **Body**: 16-20px, weight 400-600

### Component Variants

#### Button
- **Variants**: primary, secondary, ghost
- **Sizes**: sm, md, lg
- **Usage**: 14 instances across the page

#### Cards
- **TestimonialCard**: Displays client reviews with star ratings
- **FeatureCard**: Highlights service benefits with icons
- **ProcessStepCard**: Shows 3-step coaching process
- **FAQItem**: Accordion-style expandable questions

## 🛠️ Getting Started

### Prerequisites
- Node.js 18+ and npm

### Installation

```bash
# Navigate to project directory
cd cams-landing

# Install dependencies
npm install

# Start development server
npm run dev
```

The site will be available at `http://localhost:4321`

### Build for Production

```bash
# Build static site
npm run build

# Preview production build
npm run preview
```

## 📝 Content Management

All content is managed through Astro Content Collections with TypeScript validation.

### Adding a Testimonial

Create a new file in `src/content/testimonials/`:

```json
{
  "name": "Juan Pérez",
  "role": "Director de Operaciones",
  "rating": 5,
  "testimonial": "Excelente experiencia...",
  "image": "/images/testimonial-new.jpg"
}
```

### Adding a Feature

Create a new file in `src/content/features/`:

```json
{
  "title": "Nueva Característica",
  "description": "Descripción detallada...",
  "icon": "🎯",
  "order": 8
}
```

### Adding an FAQ

Create a new file in `src/content/faqs/`:

```json
{
  "question": "¿Nueva pregunta?",
  "answer": "Respuesta detallada...",
  "order": 7
}
```

## 🎯 Landing Page Sections

1. **Header**: Fixed navigation with CTA button
2. **Hero**: Main value proposition with stats
3. **Testimonials**: 6 client success stories
4. **Problem Statement**: Emotional pain points
5. **Features**: 7 service benefits
6. **Reviews**: Social proof statistics
7. **Process**: 3-step coaching methodology
8. **Target Audience**: Ideal client profiles
9. **About**: Founder credentials
10. **Final CTA**: Urgency-driven conversion
11. **FAQ**: 6 common questions
12. **Footer**: Links and final CTA

## 🚀 Performance

- **Static Site Generation**: Pre-rendered HTML for fast loading
- **Optimized Images**: Proper sizing and formats
- **Minimal JavaScript**: Only for interactive elements (FAQ accordion)
- **CSS Optimization**: Tailwind CSS purging unused styles

## ♿ Accessibility

- Semantic HTML structure
- Proper heading hierarchy (h1-h6)
- ARIA labels for interactive elements
- Keyboard navigation support
- Color contrast compliance

## 📱 Responsive Design

- **Mobile**: 375px+ (single column layout)
- **Tablet**: 768px+ (2-column grids)
- **Desktop**: 1024px+ (3-column grids)
- **Large**: 1440px+ (max-width container)

## 🔧 Customization

### Changing Colors

Edit `src/styles/global.css`:

```css
@theme {
  --color-primary: #your-color;
}
```

### Modifying Content

All content is in `src/content/` directories as JSON files.

### Adjusting Layout

Section components are in `src/components/sections/` and can be reordered in `src/pages/index.astro`.

## 📦 Tech Stack

- **Framework**: [Astro](https://astro.build) v5.17.1
- **Styling**: [Tailwind CSS](https://tailwindcss.com) v4.1.18
- **Language**: TypeScript (strict mode)
- **Content**: Astro Content Collections with Zod validation

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## 👀 Want to learn more?

Feel free to check [Astro documentation](https://docs.astro.build) or jump into the [Discord server](https://astro.build/chat).

## 📄 License

Copyright © 2024 Camila García Coaching. All rights reserved.
