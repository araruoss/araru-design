# Reader

Reader is an immersive mode with top bar, optional bottom controls, position, navigation, settings and exit. Controls can hide and return on interaction; content remains dominant.

## Reader contract

`ReaderShell` owns immersion, safe areas and lifecycle. `ReaderTopBar` provides title, format context, settings and exit. `ReaderDock` provides only the highest-value previous, next, position/progress and optional table-of-contents actions. `ReaderSettings` contains format-appropriate preferences. Controls may hide after inactivity and return on a deliberate tap, click or keyboard action; Escape exits immersion or closes the current panel.

PDF, CBZ and CBR are page-based. EPUB is flow/CFI-based. MOBI depends on the active engine. The shared contract therefore exposes `position`, `progress` and `canJump`, while labels and controls are format-specific. Page transitions are optional, must not hide content, must respect reduced motion and must not depend on touch.

Mobile preserves safe-area insets, avoids clipping during orientation changes, uses comfortable gesture targets and keeps an accessible non-gesture route to every action. Desktop and tablet may dock controls differently without changing the semantic priority.
