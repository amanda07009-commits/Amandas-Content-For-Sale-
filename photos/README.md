# Photos

Everything the site shows lives in this folder, one subfolder per category:

```
photos/
  places/
  food/
  villas/
  people/
  me.jpg        ← your portrait for the About section
  share.jpg     ← 1200×630 image shown when someone pastes your link into WhatsApp/Instagram
```

## Naming

`city-client-number.jpg`, lowercase, hyphens, no spaces:

```
photos/food/canggu-clientname-01.jpg
photos/villas/ubud-clientname-07.jpg
photos/food/canggu-clientname-clip-01.mp4
```

Same name on your laptop, in your backup, and here, so you can always find the original.

## Export settings

**Photos:** 2000 px on the long edge, sRGB, JPG quality around 80. Aim for 300–600 KB each.
Anything bigger makes the page slow on café wifi and mobile data.

**Clips:** 1080×1920 (vertical), H.264 MP4, 5–12 seconds, no sound. Keep each under 8 MB.
Optionally export one frame as a JPG and set it as the clip's `poster` so something shows while it loads.

## Adding one to the site

1. Drop the file in the right subfolder.
2. In `index.html`, find the `photos:` list in the CONFIG block and fill in an empty slot:

```js
{ category: 'food', src: 'photos/food/canggu-clientname-01.jpg', caption: 'Hero dish, from above', place: 'Canggu', ratio: '4/5', hero: true },
```

3. Save and refresh. The placeholder is replaced by your photo.

Mark three photos with `hero: true`: those become the taped prints at the top of the page.
Add an entry with `cover: true` to choose which photo fronts its category card.
