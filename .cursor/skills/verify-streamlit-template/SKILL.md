---
name: verify-streamlit-template
description: Launch blank-app's actual Streamlit starter template and prove title, starter text, docs link, reload and mobile/desktop rendering without claiming product functionality.
---
# Streamlit starter verification

## Launch
Use Python3.10+ with `python3 -m venv /tmp/blank-runtime` then `/tmp/blank-runtime/bin/pip install -r requirements.txt`. The repository requirement is unpinned; the executed proof used Streamlit1.65.0. Normal launch: `/tmp/blank-runtime/bin/python -m streamlit run streamlit_app.py`. For the helper install Node22.12+, Chrome, and `npm ci --ignore-scripts --prefix .cursor/skills/verify-streamlit-template`. Set CHROME_PATH when Chrome is not /usr/bin/google-chrome.

## Doctor
`STREAMLIT_PYTHON=/tmp/blank-runtime/bin/python node .cursor/skills/verify-streamlit-template/helpers/verify.mjs /tmp/blank-proof` begins with real installed Streamlit version and its own ephemeral loopback server's /_stcore/health. Browser rendering must then show the expected title, not just an open port. No account, secret, database, seed or external service is required. After a failed run repeat from a fresh owned instance, never reuse an unknown Streamlit session.

## Drive
The same helper command runs the real app at390/1365 and checks title, starter copy, exact docs link href, absence of Streamlit exception, no horizontal overflow/pageerrors and reload. It captures screenshots. The app only displays starter text and a link; there are no CRUD, computation or business features to drive. This is executable-template proof, not an application feature pass. The helper does not click Deploy, alter settings or open the external docs page.

## Evidence
Named output has result.json, server.log and both-width template PNGs. Inspect actual pixels. In this Linux browser the balloon emoji is a missing-glyph box despite correct DOM text; title/copy/link remain readable. Emoji appearance is unverified on actual user devices, not a reason to call all pixels perfect. No synthetic internal setters or mocks are used.

## Cleanup
Helper closes only its own browser/server; evidence survives at the named path. Confirm result.json/PNGs after exit. Each run owns a separate port/browser, no shared profile or state. Never kill Streamlit by name or remove evidence.

## Coverage and maintenance
No functional product, hosted status, external-docs availability, CI, accessibility/device, security audit or future feature behavior is established. Re-interview and expand this map when the template becomes an app. Use /maintain-verification-skill after changes, never count this template as a fully verified application.
