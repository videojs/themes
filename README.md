# Videojs Themes

Monorepo for Video.js themes :nail_care:.

## Usage

You can pull in the CSS via link tags

```html
<!-- Video.js base CSS -->
<link href="https://unpkg.com/video.js@7/dist/video-js.min.css" rel="stylesheet">

<!-- City -->
<link href="https://unpkg.com/@videojs/themes@1/dist/city/index.css" rel="stylesheet">

<!-- Fantasy -->
<link href="https://unpkg.com/@videojs/themes@1/dist/fantasy/index.css" rel="stylesheet">

<!-- Forest -->
<link href="https://unpkg.com/@videojs/themes@1/dist/forest/index.css" rel="stylesheet">

<!-- Sea -->
<link href="https://unpkg.com/@videojs/themes@1/dist/sea/index.css" rel="stylesheet">
```

Or, if you're using CSS modules in JavaScript, you can install the NPM module:

```sh
npm install --save video.js @videojs/themes
```

Then just import the files as you would other CSS.

```javascript
import 'video.js/dist/video-js.css';

// City
import '@videojs/themes/dist/city/index.css';

// Fantasy
import '@videojs/themes/dist/fantasy/index.css';

// Forest
import '@videojs/themes/dist/forest/index.css';

// Sea
import '@videojs/themes/dist/sea/index.css';
```

Once you've got the theme pulled in, you can then add the relevant class to your player! The class names are structured as `vjs-theme-${THEME_NAME}`, so `vjs-theme-city` for the city theme or `vjs-theme-sea` for the sea theme.


```html
<video id="my-player" class="video-js vjs-theme-city" ...>
```

# Building these locally

If you want to use the CSS in this repo directly instead of using one of the CDNs or the NPM-hosted version, or just do some development, you'll need to clone the repo and `build` them.

```
$ git clone https://github.com/videojs/themes videojs-themes
$ cd videojs-themes
$ npm install
$ npm run build
```

This will create a `dist` folder with the post-processed CSS in them, which you can upload right to your site. If you want to develop against these locally, you can run `npm run dev` to get a local server running a demo of all the themes on it.
