1.  **Where to fit automated tests in the Recipe project pipeline?**  
Within a GitHub Action that runs whenever code is pushed. This ensures every change is automatically validated in CI, catches regressions early, and keeps the main branch healthy without relying on manual steps.

2. **No.** End-to-end tests focus on user flows and UI interactions; verifying a function’s return value is best handled by unit tests.





