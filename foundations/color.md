# Color

Use semantic roles from `tokens/color.json`, never raw palette names in product contracts. The primitives are Deep Navy `#0A192F`, Royal Blue `#2274A5`, Cyan `#00B4D8`, Action Yellow `#FFB703`, Action Orange `#F77F00`, and neutral surfaces. Light and dark themes are composed independently; dark mode is not an inversion.

Accent is reserved for primary actions and reading progress. Royal/Cyan support links, navigation and focus. Status colors must also have text, icon or structural support and meet WCAG 2.2 AA contrast. Keep interfaces mostly neutral so covers and brand assets provide the visual energy.

## Usage

Do use `background`, `surface`, `text-primary`, `link`, `accent` and `focus-ring` semantic roles. Do not place raw palette values in application components, use accent for body text or use orange as an error color. Yellow/orange actions use `accent-foreground` (Deep Navy), never an assumed white foreground.

## Theme summary

- Light: neutral background and surfaces, Deep Navy text, Royal links, Yellow primary actions and Cyan focus.
- Dark: Deep Navy background, blue-toned surfaces, light text, Cyan links and the same controlled action accent.
