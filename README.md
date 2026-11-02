# Wardrobe Guide & Checklist

A standalone, mobile-friendly wardrobe planner that combines a personal colour guide, a shopping checklist, and an outfit builder.

## Features

- **Checklist**
  - Track recommended wardrobe pieces across trousers, shirts, shoes, belts, jackets and layers, occasion wear, gym and football, and accessories.
  - Switch between **To buy** and **Owned** views.
  - Filter checklist items by category.
  - Adjust owned quantities with the `+` and `−` controls.
  - Add custom items to the owned list.
  - View an overall owned-pieces count and progress bar.

- **Colour guide**
  - Shows recommended and less suitable colours for tops and bottoms.
  - Includes short notes explaining how each colour should be used.

- **Outfit builder**
  - Start with a top or a bottom colour.
  - See compatible colours ranked as **Best**, **Good**, **Risky**, or **Avoid**.
  - Filter suggestions to colours already marked as owned.
  - Generate a simple outfit suggestion with shoes, belt, and layering guidance.
  - Mark additional tops and bottoms as owned when needed.

- **Interface**
  - Responsive layout for mobile and desktop screens.
  - Automatically follows the operating system light/dark preference.
  - Supports an accessible, keyboard-friendly button-based interface.
  - Uses no external libraries, build tools, or network requests.

## Getting started

1. Open [`Wardrobe Guide & Checklist.html`](./Wardrobe%20Guide%20%26%20Checklist.html) in a modern web browser.
2. Open **Checklist** and use the `+` button as you acquire recommended pieces.
3. Use **Owned** to review what you have and add custom items.
4. Open **Colour guide** for colour recommendations.
5. Open **Outfits** to build combinations from colours you own.

No installation or web server is required. The file can be opened directly from the filesystem.

## Data storage

Checklist quantities and custom owned items are saved in the browser's `localStorage` under the `wg2` key. Outfit-builder ownership selections are saved separately under the `wg3` key.

This means:

- Your data remains in the browser on the device where you use the page.
- Clearing site or file storage can remove your saved selections.
- Data is not synchronized between browsers or devices.
- A different browser may show an empty checklist.

## Customization

The page content and logic are contained in the HTML file:

- Colour values are defined in the `C` object.
- Colour-guide entries are populated by the `fill(...)` calls.
- Recommended checklist items are defined in the `D` array.
- Outfit compatibility scores and explanations are defined in the `M` object.
- Styling is contained in the `<style>` block.

To customize the planner, edit those sections directly and reopen the HTML file in the browser.

## Browser support

Use a current version of Chrome, Edge, Firefox, Safari, or another browser with support for:

- JavaScript
- `localStorage`
- CSS Grid and CSS custom properties
- `prefers-color-scheme`

