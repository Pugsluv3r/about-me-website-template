# Customizing Your Website

This guide explains how to replace the profile picture, music tracks, and album covers in this template. The paths below match the files and code currently included in the repository.

## 1. Replace Your Profile Picture

1. Open the `Resources` folder.
2. Replace `PfP.jpg` with the image you want to use.
3. Keep the new image named `PfP.jpg` and in JPG format so the existing website code can find it.

The profile picture is displayed by this line near the top of `index.html`:

```html
<img class="avatar" src="Resources/PfP.jpg" alt="Profile Picture"/>
```

If you want to use a different filename or format, update the `src` path to match. For example, if your image is named `my-picture.png`, change it to `src="Resources/my-picture.png"`.

## 2. Replace the Songs

The music files are stored in the `Resources` folder:

- `Song1.mp3`
- `Song2.mp3`
- `Song3.mp3`

To replace a song, use an audio file in MP3 format and either overwrite the corresponding file or rename your new file to match one of the names above. Keep the file in the `Resources` folder.

The playlist is defined in the JavaScript near the bottom of `index.html`:

```javascript
const playlist = [
    {
        name: "first song - artist",
        src: "Resources/Song1.mp3",
        cover: "Resources/Covers/Cover1.jpg"
    },
    {
        name: "second song - artist",
        src: "Resources/Song2.mp3",
        cover: "Resources/Covers/Cover2.jpg"
    },
    {
        name: "third song - artist",
        src: "Resources/Song3.mp3",
        cover: "Resources/Covers/Cover3.jpg"
    }
];
```

For each track, edit `name` to show the song title and artist. The `src` value is the path to the audio file, and `cover` is the path to that track's album cover.

For example, to use a file named `my-song.mp3` inside `Resources`, change the track's `src` to `Resources/my-song.mp3`. The path and filename must match exactly, including capitalization.

To add another song, add another object inside the `playlist` array, following the same format and making sure the commas between objects are correct. Upload or copy the audio file into the folder named in its `src` path.

Only use music you have permission to use.

## 3. Replace the Album Covers

The album-cover images are stored in `Resources/Covers`:

- `Cover1.jpg`
- `Cover2.jpg`
- `Cover3.jpg`

Replace each image with your chosen cover, keeping the same filename and JPG format. Alternatively, change the corresponding `cover` value in the playlist in `index.html` to the new image path.

For example, if you add `my-cover.png` to `Resources/Covers`, update the relevant playlist entry to:

```javascript
cover: "Resources/Covers/my-cover.png"
```

Each playlist entry's `cover` value controls which cover appears for that song. Use a separate image path for each track if you want different covers.

## 4. Change Your Name and Other Website Text

Open `index.html` in a text editor and replace the template text with your own. For example:

- `Your site title` inside the HTML `<title>` element changes the browser tab title.
- `Your username` changes the name shown in the top navigation panel.
- `Your discord user` changes the displayed Discord username.
- The headings and placeholder paragraphs inside the `home`, `about`, `experience`, `contact`, and `Discord` sections are the content for those pages.
- The Discord invite button currently opens `https://discord.gg/`. Replace that URL in the button's `onclick` attribute with your own invite link.

The Discord icon and badge images are also in `Resources`. Their paths are referenced directly in `index.html`.

## 5. Change the Website's Appearance

Open `style.css` to edit the website's styling, including colors, spacing, sizes, and layout. Save the file and refresh the browser to see your changes.

## 6. Preview the Website

This project currently contains `index.html`, `style.css`, and resource files; it does not include a package manifest or a build command.

1. Save your changes.
2. Open the project folder on your computer.
3. Open `index.html` in a modern web browser.
4. Test the navigation and music player. If an image or song does not appear, check that its path, filename, and capitalization match the references in `index.html`.

If you make changes while the page is open, save the files and refresh the browser. If your browser has trouble loading a local audio file, run a simple local web server from the project folder or use your editor's local preview feature.

## 7. Publish the Website

The project is a static website, so it can be hosted by a static website provider. For GitHub Pages, push the project files to your GitHub repository, open the repository's **Settings**, select **Pages**, and configure deployment from the branch containing your website files. Ensure `index.html` is in the published folder. Follow GitHub's current Pages instructions if the settings have changed.

## Troubleshooting

- **An image is missing:** Confirm that the file is in the correct folder and that the path and capitalization match the code.
- **A song will not play:** Confirm that the audio file is a supported format (the included paths use MP3 files) and that its `src` path is correct.
- **The wrong cover appears:** Check the `cover` path in the playlist entry for that song.
- **Your changes do not appear:** Save your edits and refresh the browser. If needed, try a hard refresh.
