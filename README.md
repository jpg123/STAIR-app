# STAIR App

STAIR (Soft-Tissue Adjustment Intensity Ratio) is a browser-based companion for communicating cohort-level resource intensity across burn, frostbite and necrotizing fasciitis admissions. Open the [hosted app](https://jpg123.github.io/STAIR-app/STAIR-app.html) or open `STAIR-app.html` locally.

## Use

Enter counts for each diagnosis group. The app applies frozen burn-referenced cohort factors and displays relative intensity units. It does not calculate patient-level predictions, bed-day estimates or treatment effects. Do not enter identifiable patient information.

The interface is available in English, French and Spanish. Share Data shares the entered case mix and resulting cohort summary; Share App shares the app link.

## Frozen factors

The app uses the versioned FAMD artifact maintained with the companion HRU study materials. The underlying factors are Burn 1.000000, Frostbite 0.800201 and Necrotizing Fasciitis 1.279815; the interface displays them rounded to 1.00, 0.80 and 1.28. The weighted case-mix calculation is:

`(burn cases × 1.00) + (frostbite cases × 0.80) + (necrotizing fasciitis cases × 1.28)`

The app does not refit FAMD. This app-only repository does not contain the derivation analysis code or patient-level data. The underlying study used a Canadian provincial registry; the app is not a validated bedside prediction tool and should not be used for individual triage or clinical decisions.

## Files

- `STAIR-app.html`: standalone app
- `index.html`: redirect to the standalone app
- `manifest.json`, `icon.svg` and `sw.js`: progressive web app metadata and offline support

The code is provided for research and educational knowledge translation. No reuse license is included; contact the study team before adapting or redistributing the code or factors.
