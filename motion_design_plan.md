# Motion Design Selection Menu — Ninad Patwardhan Portfolio

This document contains all the animation concepts requested. You can select the specific ideas you like from each section, and I will implement them.

---

## 1. Hero Section
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Dropped Words** | "Ninad" falls first, "Patwardhan" follows shortly after, landing with a slight bounce. | CSS `translateY(-100vh)` to `0` with `cubic-bezier(0.175, 0.885, 0.32, 1.275)`. |
| **Memory Reveal** | Background "MEMORY" text appears one letter at a time, left-to-right, very slowly. | Split text into spans; staggered `opacity` animation with 0.2s delay per char. |
| **Slot Machine Dates** | 1947 and 1992–93 roll up from 0000 like a slot machine reel. | JS function cycling digits `0-9` rapidly before stopping on the target digits. |
| **Typewriter Tagline** | "Psychologist of Memory" types out live with a blinking cursor. | CSS `steps()` animation or JS character-by-character string replacement. |
| **Outward Lines** | Thin horizontal lines grow from the middle of the page toward the edges. | `transform: scaleX(0)` to `1` with `transform-origin: center`. |

---

## 2. Publications
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Snap Stamp** | REF stamps start big/rotated and "snap" into place like a rubber stamp on paper. | `scale(2) rotate(-15deg)` -> `scale(1) rotate(0)` + impact shake. |
| **Drawing Quote Border** | Left border of quote boxes draws itself top-to-bottom as you scroll. | `transform: scaleY(0)` -> `1` with `transform-origin: top`. |
| **Journal Slide-Up** | Journal name slides up into place 0.2s after the title appears. | `translateY(20px)` -> `0` with a delayed CSS transition. |
| **Word-by-Word Authors** | Author names appear one by one: "Patwardhan," [pause] "N.," etc. | Split author string into spans; staggered `opacity` reveal. |
| **Retrieve Jump** | The "Retrieve" link jumps slightly toward the mouse on hover. | CSS `:hover { transform: translateX(8px); }` or a subtle magnetic JS effect. |

---

## 3. Conferences
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Bounce Drop 📍** | Location text drops from above and bounces lightly before settling. | `translateY(-30px)` to `0` with a bounce keyframe. |
| **Year Number Flip** | Year flips through wrong numbers (9999, 2000...) before landing on the correct one. | Rapid JS cycling of digits for 0.5s before final value. |
| **Sheet Slide-In** | Each entry slides in from the left like a sheet of paper being slid onto a desk. | `translateX(-100%)` -> `0` with a slight tilt (`rotate(-1deg)`). |
| **Projector Flicker** | Title flickers briefly (blinks) like a projector warming up before becoming sharp. | `opacity` keyframes: `0 -> 1 -> 0.2 -> 1 -> 0.5 -> 1`. |
| **Hand-Drawn Border** | A thin border traces itself clockwise around the entire card. | SVG `stroke-dashoffset` animation on a rect path. |

---

## 4. Awards
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Shimmer Reveal** | A soft shimmer moves across the row, revealing it from left to right. | `linear-gradient` mask moving across the width. |
| **Color Warm-up** | Row starts grey and "warms up" to its theme color (Gold/Terra). | `filter: grayscale(1)` -> `grayscale(0)` + color transition. |
| **Clock Rewind** | Year ticks down from a higher number to the correct one (e.g., 2030 -> 2024). | JS counter function running in reverse. |
| **Landed Bounce** | Entire row gently bounces up once when it enters the screen. | `translateY(15px)` -> `0` with a small overshoot. |
| **Rotating Icon** | Medal icon rotates one full turn before settling upright. | `rotate(0)` -> `rotate(360deg)` on intersection. |

---

## 5. Talks
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Stage Spotlight** | A spotlight-shaped glow fades in from the left as the entry appears. | `radial-gradient` overlay with increasing opacity. |
| **Title Echo** | Title has a faint blurred copy behind it that fades away (the "echo"). | `::after` content with `filter: blur` and `opacity` fade. |
| **Meeting Halves** | Left and right halves of the entry slide from opposite sides and meet in middle. | `translateX(-50%)` and `translateX(50%)` meeting at `0`. |
| **Caption Slide** | Venue/location slides in from the right 0.3s after the title. | `translateX(40px)` -> `0` with a delay. |
| **Heartbeat Border** | Left border pulses once (expands/contracts) when reached. | `border-left-width` or `scaleX` pulse keyframe. |

---

## 6. Supervision
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Sprouting Dot** | Entry starts as a tiny dot and grows outward to full size. | `transform: scale(0)` -> `1` with an organic ease. |
| **Dealing Cards** | Rows appear one by one with a 150ms gap between them. | Staggered `IntersectionObserver` delays. |
| **Unfolding Paper** | Each row unfolds downward (top-to-bottom reveal). | `transform: rotateX(-90deg)` to `0` with `perspective`. |
| **Thesis Slide** | Thesis topic slides in from the right while other info is static. | `translateX(60px)` -> `0` only for the project line. |
| **Drawing Checkmark** | Checkmark icon draws its path from start point to end point. | SVG `stroke-dashoffset` path animation. |

---

## 7. Articles
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Fold Unfolding** | Article row starts folded and unfolds downward to full height. | `transform: scaleY(0)` with `transform-origin: top`. |
| **Stamp Drop Shake** | Headline drops from above and hits with a brief shake. | `translateY(-40px)` -> `0` followed by 0.2s of jitter. |
| **Ink Soaking** | Publication name starts blurry/transparent and sharpens into focus. | `filter: blur(8px) opacity(0)` -> `blur(0) opacity(1)`. |
| **Lifting Shadow** | Row lifts slightly and casts a shadow when entering view. | `translateY(-4px)` + `box-shadow` transition. |
| **Squish & Spring** | Row briefly compresses vertically then springs back to normal height. | `scaleY(0.8)` -> `scaleY(1.1)` -> `scaleY(1)`. |

---

## 8. Journey / Academic Record
| Idea | Description | Technical Implementation |
| :--- | :--- | :--- |
| **Printing Line** | Rows slide in from the left with a small delay (like a printing press). | `translateX(-30px)` -> `0` with sequential delays. |
| **Institution Typing** | Institution names appear character-by-character. | JS typewriter function per row. |
| **Clicking Years** | Date range counts up/clicks forward year by year (e.g. 2013 -> 2018). | JS interval that updates text content every 50ms. |
| **Approval Stamp** | Degree badges snap into place with a slight rotation. | `scale(1.4) rotate(15deg)` -> `scale(1) rotate(0)`. |
| **Sequenced Columns** | Positions load first, then Education loads 300ms later. | Parent container staggered delay for the two column groups. |
