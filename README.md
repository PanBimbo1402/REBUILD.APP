# REBUILD 0.8 — Clean Rebuild

Built fresh from the known-working 0.6.1 foundation. No 0.7 application code was used as the base.

## Included
- Stable, explicit Today / Training / Nutrition / Progress / Plan routing.
- Today-only sleep entry; Progress analyzes sleep; Training does not duplicate sleep logging.
- Strength, Cardio, Running, Mobility/Plyometric training tabs.
- No-run gate: no run form on days without a scheduled run; next scheduled run is shown.
- Strength rest timer Start/Resume, Stop/Pause, Reset behavior from the stable base.
- PR-anchored suggested starting weights for related strength exercises; no weight suggestions for mobility/plyometrics.
- Exercise thumbnails, movement popup, muscle targeting, cues and technique links.
- Separate Mobility Prep and Plyometric Power blocks on Today for lower/run sessions.
- Nutrition daily macros, food logging, gram-based meal prep, three meal rotations, and optional food-preference questionnaire.
- Progress: bodyweight trends, sleep trends, PR baselines, and week-over-week working-weight percentage indicators.
- Plan: program calendar, editable life context, future work shifts without a three-week limit, and life events.
- English/Spanish selection and UI translation layer; EN/ES switch.
- Adult presentation foundation for age 45+: purple accent, larger controls/text, REBUILD ADULT identity.

## QA performed before packaging
- `node --check` passed for `js/app.js` and `js/data.js`.
- 22/22 structural/regression assertions passed.
- Runtime harness exercised all five section renderers and verified Progress/Plan isolation, Nutrition meal prep, no-run gating, sleep-entry placement, life planning, and repeated routing.
- Navigation stress test cycled all five sections 50 times and ended on the correct Progress renderer.
- Major view definitions verified unique: one renderer each for Today, Training, Nutrition, Progress, and Plan.
- ZIP integrity tested after packaging.

Automated Chromium was attempted, but this environment's browser policy blocks local/file/data pages. Therefore real-device visual QA remains the final check; browser visual automation is not claimed.
