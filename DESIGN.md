---
name: CoffeeConnects
description: Coffee, conversations, and community in a warm noticeboard visual system.
colors:
  honey: "#f7ce68"
  espresso: "#30251e"
  rust: "#9a381e"
  milk: "#fff7e7"
typography:
  display:
    fontFamily: '"Bricolage", sans-serif'
    fontSize: "clamp(4rem,7.1vw,6rem)"
    fontWeight: 800
    lineHeight: 0.97
    letterSpacing: "-.035em"
  body:
    fontFamily: '"Manrope", sans-serif'
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.625
  label:
    fontFamily: '"Manrope", sans-serif'
    fontSize: "0.875rem"
    fontWeight: 600
rounded:
  poster: "3px"
  pill: "9999px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "32px"
  xl: "48px"
components:
  button-primary:
    backgroundColor: "{colors.espresso}"
    textColor: "{colors.milk}"
    rounded: "{rounded.pill}"
    padding: "16px 28px"
  button-primary-hover:
    backgroundColor: "{colors.rust}"
  status-chip:
    textColor: "{colors.espresso}"
    rounded: "{rounded.pill}"
    padding: "8px 16px"
  poster:
    backgroundColor: "{colors.espresso}"
    textColor: "{colors.honey}"
    rounded: "{rounded.poster}"
    width: "100%"
---

# Design System: CoffeeConnects

## Overview

**Creative North Star: "Community noticeboard"**

The implemented system pairs a honey field with espresso ink, oversized display lettering, and a typographic poster. Warm colors and direct invitation copy support the café's coffee, conversations, and community positioning. Visual emphasis comes from type scale, contrasting surfaces, and a slight poster tilt.

**Key Characteristics:**

- Honey background with espresso text and surfaces.
- Heavy Bricolage display lettering with Manrope supporting copy.
- Rust punctuation and primary-action hover states.
- Pill-shaped actions and status indicators alongside a nearly square poster.

## Colors

The four-color palette uses warm tones across light and dark surfaces; frontmatter contains the canonical values.

### Primary

- **Honey:** page background, poster lettering, and circular cup emblem.
- **Rust:** headline and brand punctuation, selection background, focus outlines, and primary-action hover.

### Neutral

- **Espresso:** main text, action background, poster surface, and divider strokes. Reduced opacity softens supporting text and borders.
- **Milk:** action text and supporting text on espresso surfaces.

## Typography

**Display Font:** locally hosted Bricolage, with sans-serif fallback.
**Body Font:** locally hosted Manrope, with sans-serif fallback.

### Hierarchy

- **Display:** heavy, tightly tracked invitation headline using the frontmatter display role.
- **Poster display:** weight (800), line height (1.05), tracking (-.025em). Three observed sizes are `clamp(3rem,5vw,4.7rem)`, `clamp(2.4rem,4vw,3.7rem)`, and `clamp(2.7rem,4.4vw,4.1rem)`.
- **Intro:** semibold (600), size (20px), rising to (24px) at the small breakpoint, with snug line height (1.375).
- **Body:** relaxed copy grows from (16px) to (18px) at the small breakpoint; introductory copy is constrained to (43ch).
- **Labels:** Manrope status text grows from (12px) to (14px); footer copy is (14px).

## Layout

The outer container caps at (1600px). Horizontal padding is (24px), rising to (40px) at (640px) and (64px) at (1024px). Header and footer use thin dividers and generous vertical padding.

The main area stacks by default, then uses a (1.15fr / 1fr) grid at (1024px). Its gap grows from (48px) to (56px). Vertical padding progresses from (56px) to (80px) to (96px). The centered poster caps at (520px). The footer becomes two columns at (640px).

Below (640px), the poster is level and its entrance animation is disabled. The desktop hero uses `min(740px, calc(100svh - 260px))` as its minimum height; the mobile hero has natural content height.

## Elevation & Depth

Flat color fields and translucent divider strokes organize the page. The poster is the only shadowed surface: `0 18px 36px #30251e20`. Its desktop resting rotation is (2deg).

The poster settles once over (850ms) using `cubic-bezier(.16,1,.3,1)`, from a (5deg) rotation and (12px) downward offset. Reduced-motion preferences disable animation, smooth scrolling, and the primary-action color transition.

## Shapes

The poster has nearly square corners using its radius token. Actions, the outlined status chip, and the cup emblem are fully rounded. Icons use simple stroked outlines and inline SVG.

## Components

### Buttons

The primary action is an espresso pill with milk text, semibold Manrope, and an inline arrow. Minimum height is (56px). Hover shifts its background to rust. Keyboard focus uses the shared rust outline (3px) with offset (6px).

### Chips

The status chip uses a translucent espresso border, transparent background, and a solid espresso dot. It is informational, with no interactive or selected states.

### Cards / Containers

The signature poster has honey display copy and milk supporting copy on espresso. Top and bottom bands use translucent honey dividers. Horizontal padding grows from (24px) to (32px); the central lettering block has (28px) to (36px) vertical padding.

### Navigation

The header pairs a cup outline with a bold lowercase wordmark and rust punctuation. Wordmark size grows from (20px) to (24px), with tracking (-.035em). The footer contact link is underlined and darkens its underline on hover. Links use visible keyboard focus. A skip link becomes visible when focused.

## Do's and Don'ts

### Do:

- **Do** use the four established palette tokens for surfaces, text, punctuation, and state changes.
- **Do** pair heavy Bricolage display copy with Manrope supporting copy.
- **Do** preserve visible keyboard focus and reduced-motion behavior.
- **Do** let content stack at narrow widths and keep the mobile poster level.

### Don't:

- **Don't** apply the poster shadow to every surface; the observed layout reserves it for the poster.
- **Don't** substitute pill corners for the poster's nearly square shape.
- **Don't** use the oversized display role for supporting paragraphs or status copy.
