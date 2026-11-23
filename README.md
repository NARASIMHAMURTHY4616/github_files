# Shradha's Birthday Scrapbook 💙

A static website (plain HTML, CSS and browser JavaScript). No server, database, build step or environment variables.

```text
birthday-website/
├── index.html      <- the whole site (edit the CONFIG block at the top of the <script>)
└── README.md
```

Optional, only if you want to self-host media instead of using the external links:

```text
└── assets/
    ├── photos/memory-1.jpg … memory-4.jpg
    └── music/HappyBirthday.mp3
```

## 1. Edit your content
Everything personal lives in `CONFIG` at the top of the `<script>` in `index.html`:
name, birthday, `unlockAt`, `previewKey`, music URL, Formspree endpoint, wishes, letter, notes, gift message, and the four Memories photos with captions.

## 2. Upload to GitHub
1. Create a repository (public, any name) on github.com.
2. Click **Add file → Upload files**, drag in `index.html` and `README.md` (and an `assets/` folder if you add one), then **Commit changes**.
   The file must be named exactly `index.html` and sit in the repository root.

## 3. Turn on GitHub Pages
1. Repository **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
3. After a minute, your site is at `https://NARASIMHAMURTHY4616.github.io/<your-repo-name>/` (the page shows the link). The site does not hardcode any repository name.

## 4. Photos and music
- The four Memories photos and the music load from your existing `raw.githubusercontent.com` links. Those repositories must be **public**, otherwise the files won't load.
- To self-host instead: download the files, put them in `assets/photos/` and `assets/music/`, and change the `src` / `music` values in `CONFIG` to relative paths such as `"assets/photos/memory-1.jpg"`. Only do this after the files really exist in the repo.

## 5. Test the wish form (Formspree)
1. Open your published site with the preview link (see below), go to **Write**, type a wish and press **Send**.
2. The button shows "Sending your wish…" and is disabled. The folding-note and star animation plays only after Formspree answers with success.
3. Check your Formspree dashboard (Submissions) and email. The first time, Formspree may ask you to confirm your email address.
4. To test the failure message, turn on airplane mode and press Send: you should see a friendly error and be able to retry.
5. In your Formspree form settings you can restrict allowed domains to `narasimhamurthy4616.github.io`.
Formspree only receives wishes. There is no public database, so the Wishes scene uses the wishes listed in `CONFIG.wishes`.

## 6. Countdown and preview mode
- The site stays locked until `2026-11-26T00:00:00+05:30` (12:00 AM India time), which is the same instant worldwide.
- To preview before then, open `https://…/<your-repo-name>/?preview=YOUR_KEY`, where the key is `CONFIG.previewKey`. **Change it from the default before sharing the link.**
- The countdown uses the visitor's device clock. Anyone can change their clock, or open the page source, to get in early. A purely client-side lock cannot be made secure.
