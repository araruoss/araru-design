# Color contrast validation

The token contract defines explicit foregrounds for actions and text. Before release, validate at least these pairs with a WCAG 2.2 AA checker:

| Pair | Context | Requirement |
| --- | --- | --- |
| `text-primary` on `background` | Body copy and headings | 4.5:1 for normal text |
| `text-secondary` on `surface` | Supporting copy | 4.5:1 for normal text |
| `accent-foreground` on `accent` | Primary action | 4.5:1 for normal text |
| `link` on `background` | Text links | 4.5:1 for normal text |
| `text-inverse` on `danger` | Destructive action | 4.5:1 for normal text |
| `focus-ring` around controls | Keyboard focus | Clearly visible and not color-only |

Contrast must be checked independently in Light and Dark. Automated token checks do not replace keyboard and screen-reader review.
