wonder nest
A small, friendly learning website for word meanings and number maths. It is a standalone static site: no sign-in, server, framework, build step, or general web search.

What it does
	•	Looks up one English word at a time and shows up to three suitable definitions.
	•	Solves arithmetic expressions and shows the calculation steps. It supports `+`, `-`, `×`/`*`, `÷`/`/`, brackets, powers, percentages, and square roots, plus phrases such as “12 times 3” and “25% of 80”.
	•	Rejects links, email addresses, rude/explicit terms, and inputs outside those two learning tasks.
	•	Keeps maths calculations in the browser. Word lookups use the public Dictionary API at `dictionaryapi.dev`, so an internet connection is needed for definitions.

The safety filter is a basic input/output filter, not a guarantee that every inappropriate term or definition can be caught. This site is deliberately limited and does not provide a general-purpose chatbot or web browser.

Files
	•	`index.html` — the complete website (HTML, CSS, and JavaScript in one file).
	•	`README.md` — this guide.

Run locally
Open `index.html` in a modern browser. Maths works offline; word meanings require internet access.

Publish with GitHub Pages
	1.	Create a GitHub repository and add `index.html` and `README.md` to its top level.
	2.	In the repository, open Settings → Pages.
	3.	Under Build and deployment, choose Deploy from a branch, select the `main` branch and `/ (root)`, then save.
	4.	Wait for GitHub Pages to finish publishing. The site will appear at the URL shown in the Pages settings.

No build command is needed. Anyone who can access the published Pages URL can open the site; the repository itself may be public or private depending on your GitHub plan and settings.
