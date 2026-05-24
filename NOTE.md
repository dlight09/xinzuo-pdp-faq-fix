## What I picked

Bundle Builder product-card accessibility: keyboard users could tab to knife cards, but Enter/Space did not select them.

## Why it's the highest-impact thing here

The Bundle Builder is a conversion path for multi-item orders and tiered discounts. If a shopper relies on keyboard navigation, the main interaction was exposed as a button but only worked with pointer input. That blocks selection, checkout progress, and fails WCAG keyboard operability expectations.

## What I did

I kept the existing card UI and added the missing behavior only. Bundle cards now listen for `keydown`, treat Enter and Space like click activation, preserve `aria-pressed`, and show a visible `:focus-visible` ring so keyboard users can see which card will be selected.

## What I'd do next

I would test the pushed theme on a Shopify dev store with a screen reader, then consider making the cards real checkbox controls if the bundle rules become more complex.
