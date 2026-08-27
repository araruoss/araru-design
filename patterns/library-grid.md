# Library grid

Use cover-led items with responsive columns and stable aspect ratios. Do not wrap every work in a visually heavy card.

Use a fluid grid: choose the largest number of columns that preserves a comfortable minimum cover width, then let the available content width determine the result. The contract does not prescribe fixed columns. Titles and authors may wrap to multiple lines without changing cover ratio; long content must not overlap neighboring items.

Filters and sort live in a compact toolbar on expanded screens. On compact screens they open in a sheet or drawer with an explicit Apply and Reset. Support library, category, series, format, favorite, completed and ordering filters. Pagination or infinite loading must preserve scroll position; virtualization is allowed and must not require all items to be mounted.

Work states include default, hover, focus, pressed, selected, loading, favorite, progress, completed, unavailable and missing cover. Hover-only actions are supplementary; primary reading and selection actions remain available to keyboard and touch users.
