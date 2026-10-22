# NavBarz brand

## The idea

The mark is the same window three times. The same three destinations sit along the bottom, then stand
up as a rail, then widen into a drawer with room for labels. Nothing else changes — same window, same
list, same selection. That is the whole product in one shape, and it is why the mark is a strip rather
than a symbol: a single frame could only show one mode, and one mode is not what NavBarz does.

Orange marks the **selected** destination, which is the job colour does in a real navigation bar. It is
the same destination in all three frames. Do not recolour the other destinations.

## Files

| File | Use it for |
|---|---|
| `navbarz-mark.svg` | the primary mark — README hero, docs headers, slides. 416×120 |
| `navbarz-mark-reverse.svg` | the same two colours on a dark field |
| `navbarz-mark-mono.svg` | one colour, on light |
| `navbarz-mark-white.svg` | one colour, on dark |
| `navbarz-lockup.svg` | mark plus wordmark, horizontal. The default for anywhere the name is not already next to it |
| `navbarz-lockup-mono.svg` | one-colour lockup |
| `navbarz-lockup-white.svg` | reversed lockup |
| `navbarz-lockup-stacked.svg` | the strip above the wordmark, both the same width. For square-ish spaces |
| `navbarz-icon.svg` | the square sibling — avatars, app lists, anywhere 3.5:1 does not fit. 256×256 |
| `navbarz-icon-reverse.svg` | the same two colours on a dark field |
| `navbarz-icon-mono.svg` / `-white.svg` | one colour, on light and on dark |
| `navbarz-icon-tile.svg` | the same icon on a solid ink field, for favicons and app icons |
| `navbarz-icon-tile-small.svg` | the small-size cut: destinations dropped, bands only |
| `web/` | `favicon.ico`, the PNG icon set, `site.webmanifest`, and `head-snippet.html` to paste |

The square icon is not a crop of the strip. It is one window carrying the chrome on **both** edges —
the same vocabulary, compressed into a square, because a 3.5:1 strip is illegible as an avatar.

## Colour

| Token | Hex | Role |
|---|---|---|
| Ink | `#101114` | the mark, the wordmark, dark fields |
| Signal | `#FF5A1F` | the selected destination, and nothing else |
| Paper | `#FFFFFF` | the reversed mark; the chrome bands are transparent, so they take whatever is behind |

The bands are real holes (`fill-rule="evenodd"`), not white shapes. That is deliberate: the mark sits on
any background without a white box around it. The one exception is `navbarz-icon-tile*.svg`, which is
opaque because favicons and app icons need a solid field.

Signal on Ink is 6.3:1. Signal on white is 3.0:1 — fine for a graphic element, **not** for body text.

## Clear space and minimum size

Clear space on all four sides is the height of one chrome band — 22% of the mark's height. Nothing else
goes in it.

| Asset | Minimum |
|---|---|
| `navbarz-mark` | 240px wide. Below that the drawer labels close up |
| `navbarz-lockup` | 200px wide |
| `navbarz-icon` | 32px |
| `navbarz-icon-tile-small` | 16px |

Below 32px use the small cut. The destinations are the first thing to go; the bands carry the mark.

## Type

The wordmark is **JetBrains Mono Bold**, outlined to paths — no font is needed to render it, and none is
redistributed here. JetBrains Mono is SIL OFL 1.1, which permits this use. Tracking is tightened 7.8% of
the cap height; the glyphs are otherwise unmodified.

Lowercase `navbarz`, always. It matches the coordinate people actually type:
`dev.parez.navbarz:navbarz`.

## Misuse

- Do not recolour Signal, or apply it to more than one destination per frame.
- Do not reorder the frames. Bar, rail, drawer is the resolution order the SDK actually uses.
- Do not use one frame on its own as the logo — one frame is one mode, which is the opposite of the point.
- Do not add a gradient, a shadow, a stroke or a container.
- Do not stretch. The strip is 416×120 and the icon is square; scale proportionally.
- Do not set the wordmark in another face, or in mixed case.

## Not covered

Trademark clearance has not been done. Run a proper search — trademark databases and reverse image
search — before relying on this commercially.

`sample/iosApp/iosApp/Assets.xcassets/AppIcon.appiconset/app-icon-1024.png` is still the stock Compose
Multiplatform template icon. Replacing it with `web/icon-512.png` upscaled, or a 1024px render of
`navbarz-icon-tile.svg`, is a one-line change nobody has made yet.
