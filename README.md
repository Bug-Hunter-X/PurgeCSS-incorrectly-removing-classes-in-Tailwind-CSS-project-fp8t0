# PurgeCSS Incorrectly Removing Classes in Tailwind CSS Project

This repository demonstrates an uncommon bug where PurgeCSS, despite seemingly correct configuration, removes necessary Tailwind CSS classes from the production build. This results in missing styles and broken layout.

## Bug Description

The project uses Tailwind CSS with PurgeCSS for production optimization. However, some dynamically generated or conditionally rendered classes are being removed by PurgeCSS, even though they should be included based on the purge configuration. The bug isn't readily apparent due to the complexity of the class generation or conditional rendering. 

## Reproduction

1. Clone this repository.
2. Install dependencies: `npm install`
3. Build the project: `npm run build`
4. Observe that certain elements are missing styles in the production build due to the missing classes.

## Solution

The solution involves carefully reviewing the PurgeCSS configuration, including the content section. Ensuring the paths to all possible template files and components are specified accurately. If dynamic class generation is involved, exploring alternative strategies for handling class names during the build process might be necessary. 
