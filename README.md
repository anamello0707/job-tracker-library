# Job Tracker skills library

The list of skills, types of work and industries that the Job Tracker app uses to compare job ads with CVs, in English and Norwegian.
Every installed Job Tracker downloads `skills-library.json` from here (at most once a day), so adding concepts here reaches all users without a software update.

## Format

```json
{ "category": "skill", "name": "Stakeholder management", "terms": ["stakeholder", "interessent"] }
```

- `category`: `skill`, `work` (type of work) or `industry`.
- `name`: shown in the app (English).
- `terms`: lower-case words or short phrases in English and Norwegian. A term also matches longer words that start with it ("kraft" finds "kraftsektoren"). Add `$` at the end to match the whole word only ("power$" does not match "powerful").

Keep the file valid JSON. If the app can't read it, it keeps using the last good copy.
