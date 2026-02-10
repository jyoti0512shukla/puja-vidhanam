# Sadhana app – formatted puja JSON

These JSON files in the **repo root** are for the [Sadhana](https://github.com/your-org/Sadhana) app’s **remote puja** feature. Same content as the LaTeX in `pujas/`, in the app’s schema so it can load pujas from this repo without an app update.

## Files (app schema)

| File | Purpose |
|------|--------|
| `pujas-catalog.json` | Catalog list (id, name, deity, occasion, category, duration, difficulty, available). |
| `sriramanavami-puja.json` | Full puja detail (sections, steps, mantras, offerings). |
| `ganesh-puja.json` | Full puja detail. |
| `shiva-puja.json` | Full puja detail. |

## How the app uses this repo

1. In the app: **Settings → Puja → Remote catalog URL** set to the **raw base URL** of this repo, e.g.  
   `https://raw.githubusercontent.com/raviprakashmishra/puja-vidhanam/master/`
2. The app requests `pujas-catalog.json` and `{id}.json` from that URL.
3. To add a new puja: add a new `<id>.json` here and an entry in `pujas-catalog.json`, then push. No app release needed.

Do not remove these JSON files if you want the Sadhana app to keep loading pujas from this repo.
