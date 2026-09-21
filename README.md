# Sunny Pines Golf

A playable 3D golf game that runs in a desktop or mobile browser. Two 18-hole courses, three golfers,
three-click swing, stroke play scoring with penalty-area, lost-ball and unplayable-ball relief,
saved progress, experience and levels.

Everything is in one file: `index.html`.

## Play it

Hosted version: `https://<your-github-username>.github.io/<your-repo-name>/`

## Put it on GitHub Pages

1. Create a new **public** repository on GitHub.
2. Upload `index.html` to the root of the repository (drag and drop works: "Add file" then "Upload files").
3. Open **Settings**, then **Pages** in the left menu.
4. Under "Build and deployment" choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then **Save**.
5. Wait about a minute and open the address GitHub shows at the top of that page.

To publish a new version later, upload the new `index.html` over the old one. Players may need to
refresh once (hold Shift and press reload) to get past the browser cache.

## Notes for players

- Progress (round in progress, level, records, settings) is saved in the browser it was played in.
  It does not move between devices, and it is separate from any other copy of the game.
- The page is about 6 MB because the character models are inside the file. The first load takes a few
  seconds; after that the browser caches it.
- Controls are listed in the game under "How to play". On a phone, tap to swing and drag to aim.

## What it is built from

- Rendering: [three.js](https://threejs.org) r128 (MIT licence), loaded from cdnjs.
- Fonts: Bricolage Grotesque and Atkinson Hyperlegible from Google Fonts (open licences).
- Golfers and golf swing animations: characters and motions from [Adobe Mixamo](https://www.mixamo.com).
  Check Adobe's Mixamo terms before publishing: they allow using the characters and animations in your
  own projects, but there are limits on redistributing the asset files themselves. If that matters for
  a public repository, replace the models with your own or with assets that allow redistribution.
- Physics, course design, rules, sound and everything else: written for this project, no external data.

## Rules implemented

Stroke play under the Rules of Golf (2023 edition), covering: stroke and distance for out of bounds and
lost balls (Rule 18.2), penalty area relief including lateral relief from red penalty areas (Rule 17.1d),
and the unplayable ball options including the extra option in a bunker (Rules 19.2 and 19.3).
Not implemented: provisional balls, embedded ball relief, abnormal course conditions, match play.
A casual "gimme" option inside 3 ft can be switched off in Settings; holes finished that way are marked
with a G on the scorecard and are excluded from records.
