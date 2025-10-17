# Week 2 Project: Build the charity: water Landing Page
To get started, create a new Codespace from this repo.

In this Project, you’ll transform your Canva mockup into a fully functional landing page using HTML and CSS. This is your chance to take your creative concept — with your brand visuals, your messaging, and your imagery — and make it real. You'll build a site that not only looks great, but also educates, inspires, and drives action.

With help from AI to jumpstart your layout, you'll focus on structuring your content, applying your brand style, and creating a polished final product that reflects your vision. By the end of this Project, you’ll have a live, interactive page deployed to the web. You can share this work when you want to showcase your technical skills and your passion for digital storytelling. 

## charity: water Brand Colors & Fonts

### Primary Colors:
- Yellow:     `#FFC907`
- Blue:       `#2E9DF7`

### Secondary Colors:
- Light Blue: `#8BD1CB`
- Green:      `#4FCB53`
- Orange:     `#FF902A`
- Red:        `#F5402C`
- Dark Green: `#159A48`
- Pink:       `#F16061`

### Fonts:
- Proxima Nova
- Avenir

## Troubleshooting: "gpg failed to sign the data"

If you see an error like "gpg failed to sign the data" when committing, Git is trying to create signed commits but can't access a usable GPG key in this Codespace/devcontainer. Here are simple, safe steps to resolve it.

- Quick check (already run for you):
	- Git may have `commit.gpgsign=true` and a `gpg.program` configured by the environment. That means commits are signed automatically.

- Common fixes:
	1. Use a local signing key (recommended if you know how)
		 - Generate/import a GPG key inside the Codespace and tell Git which key to use:
			 - `gpg --full-generate-key` (choose defaults) or import an existing key with `gpg --import mykey.asc`.
			 - `git config --global user.signingkey <KEYID>` (replace <KEYID> with the key shown by `gpg --list-secret-keys --keyid-format LONG`).
			 - Ensure pinentry works in the container (some environments need extra setup).

	2. Make Git stop signing commits in this Codespace (safe quick workaround)
		 - If you don't want signed commits from this environment, run:
			 - `git config commit.gpgsign false`

	3. If your workspace sets a custom gpg.program (like `gh-gpgsign`) and signing still fails
		 - That helper may require additional authentication or keys stored outside the Codespace. Using the workaround above or configuring a local key is easiest for beginners.

- Extra tips for Codespaces / devcontainers:
	- You may need to set `export GPG_TTY=$(tty)` in your shell before signing so interactive pinentry works.
	- If pinentry is missing, install a simple pinentry package (`pinentry-curses` or `pinentry-tty`) in the container.

If you'd like, I can:
- show the exact git/gpg config in this Codespace and suggest the smallest command to fix it, or
- add a one-line commit to disable signing for this repo so you can continue committing immediately.
