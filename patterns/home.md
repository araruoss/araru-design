# Home

Use optional sections: Continue Reading, Recently Added, Your Series, Favorites and Libraries. Let content determine which sections appear.

## Composition

1. Continue Reading (highest priority when present).
2. Recently Added.
3. Series and Favorites according to relevance.
4. Libraries as a navigation entry point.

Each section has a heading, optional `View all` action, a `MediaRail`, and a section-level state. With fewer items than the rail capacity, do not add filler. With many items, keep the rail horizontally navigable and expose `View all`.

## Responsive and failure behavior

Desktop uses multiple rails in the content column; tablet reduces rail density; mobile uses one predictable item size and touch scrolling. Keyboard users move into a section heading, then through items with Tab or the rail's arrow model. A failed section becomes an inline retryable error and does not block other sections or the shell. Loading uses a rail skeleton; empty sections may be omitted or use the shared empty-state pattern.
