# STAIR App

STAIR (Soft-Tissue Adjustment Intensity Ratio) is a browser-based knowledge-translation tool for communicating diagnosis-specific hospital resource requirements across burn, frostbite and necrotizing fasciitis admissions.

Use the live app at <https://jpg123.github.io/STAIR-app/STAIR-app.html> or open [`STAIR-app.html`](./STAIR-app.html) locally.

## Languages and sharing

The interface is available in English, French and Spanish. The selected language is saved locally in the browser. **Share Data** creates a text summary of the entered case mix, weighted intensity and repository link. **Share App** shares the hosted app URL. Where the browser supports the Web Share API, the native share sheet is used; otherwise the app copies the share text to the clipboard. No patient-identifiable information should be entered.

## What the app does

The app applies frozen, burn-referenced cohort intensity factors to a case mix and reports relative intensity units:

`STAIR case-mix burden = (burn cases × 1.00) + (frostbite cases × 0.62) + (necrotizing fasciitis cases × 1.80)`

The factors are frozen cohort-level outputs from the offline STAIR resource-intensity derivation. Burn is the reference level of 1.00. The app does not claim to perform FAMD, PCA or any other re-estimation in the browser. The outputs communicate relative cohort burden; they are not bed-day estimates or estimates of individual patient length of stay, mortality or treatment effect.

## Inputs represented by the derivation

The underlying resource-intensity construct uses prespecified admission-level and utilization variables: hospital length of stay, ICU admission, ICU days, procedure count, PRBC transfusion exposure, PRBC units, amputation, grafting and free-tissue transfer. The app displays frozen cohort factors and does not refit or re-estimate weights in the browser. The exact offline derivation method, preprocessing and validation must be documented with the accompanying research package.

## Interpretation and limitations

- This is a cohort-level planning and knowledge-translation tool.
- It must not be used for individual triage, bedside prediction, clinical decision-making or funding allocation.
- The factors were derived from a Canadian provincial registry of 1,680 adult admissions from 2004-2024.
- The derivation is observational and may reflect measured and unmeasured differences in diagnosis, case mix and local practice.
- External validation, prospective evaluation and stakeholder/workflow testing are required before operational use.

## Reproducibility

The app is intentionally static and uses frozen factors so that the displayed values do not change when the app is opened. The study submission package documents the derivation, cohort comparisons, diagnostics and limitations. Changes to the factors require a new offline derivation, versioned artifact and corresponding update to the manuscript and supplemental material.

## License and contact

This repository is provided for research and educational knowledge translation. Please contact the corresponding study team before adapting the factors for institutional use.
