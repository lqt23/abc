# Folio: put it on your iPhone

Folio is a web app. To install it on an iPhone, it needs to be on the web at an `https://` address once. After that it runs from your home screen, full-screen and offline. The free way to do this is GitHub Pages, which takes about 10 minutes and needs no coding.

## 1. Put the files online (GitHub Pages, free)

Do this on a computer:

1. Unzip `folio-app.zip`. You'll get a folder with `index.html`, `sw.js`, `manifest.webmanifest` and the folders `fonts`, `icons` and `vendor`.
2. Make a free account at https://github.com if you don't have one.
3. Click **+** (top right), then **New repository**. Name it `folio`, leave it **Public**, and click **Create repository**.
4. On the next page, click **uploading an existing file**. Drag in **everything inside** the unzipped folder (the files *and* the three folders, not the outer folder itself). Click **Commit changes**.
5. Go to **Settings → Pages**. Under *Branch*, choose **main** and **/ (root)**, then click **Save**.
6. After a minute or two the page shows your address, something like `https://YOUR-NAME.github.io/folio/`.

(Netlify Drop at https://app.netlify.com/drop is another option: drag the unzipped folder onto the page and you get a link straight away.)

## 2. Install on the iPhone

1. Open that address in **Safari**. It has to be Safari for the home-screen icon to work properly.
2. Tap the **Share** button, then **Add to Home Screen**, then **Add**.
3. Open **Folio** from the home screen. Open it once while you're online so it saves itself for offline use.

## 3. Adding books on iPhone

- Download an EPUB in Safari. It goes to the **Files** app, under *Downloads*.
- In Folio, tap **Add books → Choose File** and pick it.
- Good free sources: https://standardebooks.org and https://www.gutenberg.org
- Books bought from Apple Books, Kindle and similar stores are DRM-locked and won't open.

## What makes Folio different

- **Look back, spoiler-free.** Press and hold a name, then tap *Look back*. You'll see where that person first appeared and their most recent moments, searching only the pages you've already read. Tap a mention to jump there, then *Back to your page*. The clock icon lists every name you've met so far.
- **Previously…** Open a book after 6 or more hours away and you get the last passage you read, plus the names that featured lately.
- **Finish by a date.** Folio learns your own reading speed as you turn pages. In Contents, pick a *Finish by* date and it tells you how many minutes a day to read. The footer shows the time left in each chapter at your pace.
- **Ambience.** Rain, fireside, ocean or soft brown noise, generated on the phone (it works offline), with a fade-out timer. On iPhone, turn the silent switch off to hear it.

## Good to know

- Your books and reading positions are stored **inside the home-screen app on that phone**. They aren't synced to other devices, and deleting the app from the home screen deletes its books.
- The copy you open in Safari and the home-screen copy have separate libraries. Use the home-screen one.
- **Updating:** upload the new files to the same GitHub repository, replacing the old ones (your books and reading positions stay on the phone). The app picks up the change the next time you open it while online (sometimes the time after that).
- Not possible for home-screen web apps on iOS: appearing in the Share sheet's "Open in…" list, or being listed in the App Store. Getting into the App Store would need an Apple developer account ($99/year) and a Mac with Xcode to wrap the app.

## What's in the folder

| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `sw.js` | Service worker that makes it work offline |
| `manifest.webmanifest` | App name, icon and colours for install |
| `icons/` | Home-screen icons |
| `fonts/` | Literata, Inter and Atkinson Hyperlegible, bundled so they work offline (SIL Open Font License) |
| `vendor/jszip.min.js` | Opens EPUB files (MIT licence) |
