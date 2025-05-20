Anthony Georgis

1.  **Where to fit automated tests in the Recipe project pipeline?**  
Within a GitHub Action that runs whenever code is pushed. This ensures every change is automatically validated in CI, catches regressions early, and keeps the main branch healthy without relying on manual steps.

2. **No.** End-to-end tests focus on user flows and UI interactions; verifying a function’s return value is best handled by unit tests.

3. Navigation mode: Runs a fresh page load and measures load‑time metrics (FCP, LCP, TTI, etc.). It can’t capture user interactions or later DOM changes. Snapshot mode: Takes a snapshot of the current DOM state and runs checks (primarily accessibility/SEO)

4. Possible improvements based on the Lighthouse report
- **Improve performance**  
  Minify JavaScript / CSS files, preload the main hero image, and lazy-load the other images. These fixes address the red flags for Largest Contentful Paint and “unused code.”
- **Fix accessibility issues**  
  Raise text-to-background contrast, add ARIA labels to all custom buttons, and supply missing alt text or form labels. This clears the color-contrast and “button lacks accessible name” errors.
- **Strengthen SEO & best practices**  
  Add unique `<title>` and `<meta description>` tags for every page, include basic product JSON-LD, and replace vague link text with descriptive wording. This tackles the red marks in the SEO and best-practice sections.