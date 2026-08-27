# ADR 002: Reader is a separate shell

- Status: Accepted
- Problem: Library navigation chrome competes with reading focus.
- Decision: Reader owns a separate shell with its own top bar, dock, settings and exit path.
- Reason: Immersion, format-specific controls and lifecycle behavior differ materially from browsing.
- Alternatives: reuse the library shell, fullscreen a details page.
- Platform impact: All clients share the contract; platform controls may adapt to window size and input method.
