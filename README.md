# Paradise Nursery Shopping Cart (e-plantShopping)

A React + Redux single-page shopping cart application for **Paradise Nursery**, a houseplant
nursery. Built as the final project for the Coursera React course: customers browse plants by
category, add them to a cart, and manage quantities before checkout.

## Live Demo

- Deployed application (GitHub Pages): https://chunheixwx.github.io/e-plantShopping/
- Public repository: https://github.com/chunheixwx/e-plantShopping

## Features

- **Landing page** – greenhouse background image, company introduction, company name
  ("Paradise Nursery") and a **Get Started** button that opens the product listing.
- **Product listing** – 30 houseplants grouped into 5 categories (Air Purifying, Aromatic
  Fragrant, Insect Repellent, Medicinal, Low Maintenance), each card showing a thumbnail,
  name and price with an **Add to Cart** button that adds the item, disables itself and
  increments the navbar cart count.
- **Header / navbar** – shown on the product listing and cart pages with links to Home
  (Paradise Nursery), Plants and a cart icon that dynamically displays the total item count.
- **Shopping cart** – total cart amount, total number of plants, per-item thumbnail / name /
  unit price / line total, increase & decrease quantity buttons, per-item delete, a
  **Checkout** button that shows "Coming Soon", and **Continue Shopping** back to the listing.
- **State management** – a Redux Toolkit slice (`CartSlice.jsx`) wired through `store.js`
  with `addItem`, `removeItem` and `updateQuantity` reducers, consumed via `useSelector` /
  `useDispatch`.

## Tech Stack

- React 18 + Vite 5
- Redux Toolkit (`@reduxjs/toolkit`) + `react-redux`
- Plain CSS (per-component stylesheets)

## Getting Started

```bash
npm install
npm run dev        # development server
npm run build      # production build to dist/
npm run preview    # serve the production build on port 4173
```

## Key Files

| File | Purpose |
| --- | --- |
| `src/App.jsx` | Landing page (company name + Get Started) and page switching |
| `src/App.css` | Landing background image and layout styles |
| `src/AboutUs.jsx` | Company introduction paragraphs |
| `src/ProductList.jsx` | Navbar, category grid, Add to Cart, live cart count |
| `src/CartItem.jsx` | Shopping cart page (totals, quantity, delete, checkout) |
| `src/CartSlice.jsx` | Redux cart slice (add / remove / updateQuantity) |
| `src/store.js` | Redux store configuration |

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the app and publishes
`dist/` to the `gh-pages` branch; GitHub Pages serves it at the live demo URL above.