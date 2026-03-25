# Harmonium Chord Guide — SPEC.md

## 1. Project Overview
- **Name**: Harmonium Chord Guide
- **Type**: Interactive single-page web app
- **Core Functionality**: Visualize how to play chords on a harmonium keyboard
- **Target Users**: Musicians learning harmonium chords

## 2. Keyboard Range
- **Start Note**: C (leftmost key)
- **End Note**: F (rightmost key, 3.5 octaves higher)
- **Calculation**: 3 octaves (36 keys) + half octave (5 keys: C, C#, D, D#, E, F) = 41 keys total
- **Note Layout**: Standard piano layout (white: C D E F G A B, black: C# D# F# G# A#)

## 3. Visual & Rendering Specification

### Scene Setup
- Single-page HTML application
- Centered vertical layout
- Keyboard positioned prominently at center

### Art Direction — Hindi Boho Artistic
- **Color Palette**:
  - Background: Warm cream/parchment (#F5F0E6) with subtle texture
  - Keyboard white keys: Ivory (#FFFEF5) with slight warmth
  - Keyboard black keys: Rich dark wood (#2A1810)
  - Accent color: Terracotta/rust (#C75D3A), Marigold (#E8A838), Sage green (#7A9E7E)
  - Active note highlight: Warm gold glow (#FFD700) with radial gradient
- **Typography**:
  - Title: Handwritten/brush style feel (Playfair Display or similar serif)
  - Chord labels: Clean modern (Inter)
- **Decorative Elements**:
  - Subtle mandala or paisley-inspired corner decorations (SVG)
  - Warm gradient overlays
  - Soft drop shadows on keys

### Keyboard Styling
- White keys: Rounded bottom corners, ivory gradient
- Black keys: Shorter, wider, slight 3D bevel effect
- Active notes: Golden glow effect with pulse animation
- Key labels: Note names displayed on white keys

## 4. Interaction Specification

### Chord Selection
- Display chords as styled buttons in a grid/flex layout
- **Chords to include**:
  - Major: C, D, E, F, G, A, B
  - Minor: Cm, Dm, Em, Fm, Gm, Am, Bm
  - Seventh: C7, D7, E7, F7, G7, A7, B7
  - Minor Seventh: Cm7, Dm7, Em7, Fm7, Gm7, Am7, Bm7

### Chord Button Behavior
- On hover: Slight scale + color shift
- On click: Highlight the notes on keyboard, show chord name prominently
- Active state: Button stays highlighted while chord is selected

### Note Indicators
- When chord selected:
  - Corresponding keys light up with golden glow
  - Non-chord keys dim slightly
  - Smooth fade-in transition (300ms ease-out)

## 5. Chord Formulas
- **Major**: Root, +4 semitones, +7 semitones
- **Minor**: Root, +3 semitones, +7 semitones
- **Seventh**: Root, +4, +7, +10 semitones
- **Minor Seventh**: Root, +3, +7, +10 semitones

## 6. Layout Structure
```
┌──────────────────────────────────────┐
│     🪕 Harmonium Chord Guide         │  ← Title
├──────────────────────────────────────┤
│                                      │
│    ┌─────────────────────────────┐   │
│    │                             │   │
│    │      KEYBOARD (41 keys)    │   │  ← Main visual
│    │                             │   │
│    └─────────────────────────────┘   │
│                                      │
│    ┌───┐ ┌───┐ ┌───┐ ┌───┐           │
│    │C  │ │D  │ │E  │ │F  │  ...      │  ← White key labels
│    └───┘ └───┘ └───┘ └───┘           │
│                                      │
├──────────────────────────────────────┤
│  [ C ] [ D ] [ E ] [ F ] [ G ] ...   │  ← Chord buttons grid
│  [ Cm] [ Dm] [ Em] [ Fm] [ Gm] ...   │
│  [ C7] [ D7] [ E7] [ F7] [ G7] ...   │
└──────────────────────────────────────┘
```

## 7. Acceptance Criteria
- [ ] Keyboard displays exactly 41 keys (C to F, 3.5 octaves)
- [ ] White keys properly spaced with black keys positioned correctly
- [ ] All listed chords calculate correct notes
- [ ] Clicking a chord highlights correct keys with visual feedback
- [ ] Boho/Hindi artistic aesthetic is evident but clean
- [ ] Responsive: works on desktop and tablet
- [ ] No external dependencies except Google Fonts
