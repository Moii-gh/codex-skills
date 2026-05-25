---
name: universal-premium-ui-style
description: Apply a polished premium dark minimal UI aesthetic when creating, editing, redesigning, or improving user interfaces across web apps, mobile apps, desktop apps, dashboards, admin panels, AI chat interfaces, settings screens, forms, menus, modals, widgets, landing pages, and prototypes. Use for UI work unless the user explicitly requests a different style or the existing product design system must be preserved.
---

# Universal Premium UI Style

## Operating Rules

Apply this style automatically for UI work. Preserve the product's functionality, architecture, platform conventions, accessibility, and existing design system where present. Improve toward a premium dark minimal direction without copying or naming any specific existing product.

The result should feel product-ready: modern, calm, focused, spacious, readable, consistent, and practical. Avoid generic templates, default framework styling, visual noise, childish decoration, random color choices, cramped layouts, and unfinished states.

## Visual System

- Use a dark foundation: near-black, graphite, dark navy, or deep charcoal backgrounds.
- Layer surfaces with subtle contrast: primary panels slightly lighter than the background, secondary cards softer and quieter.
- Use low-opacity borders, restrained shadows, and gentle elevation to separate layers.
- Use high-contrast text without relying on pure white everywhere; keep secondary text muted but readable.
- Prefer one restrained accent family such as cool blue, violet-blue, or cyan-blue. Do not scatter unrelated accent colors.
- Use soft red for errors, calm green for success, and muted amber for warnings.
- Avoid harsh neon, rainbow gradients, saturated decoration, and flat black/white contrast without depth.

## Typography

- Use modern system typography: `Inter`, `SF Pro Display`, `system-ui`, `-apple-system`, `Segoe UI`, `Roboto`, sans-serif for web; native system fonts for mobile and desktop unless the project already defines fonts.
- Create a clear hierarchy with a small set of font sizes and weights.
- Keep headings confident but not oversized without purpose.
- Make body text comfortable to read; keep muted text accessible.
- Use medium-weight labels for buttons and important controls.
- Avoid decorative fonts unless explicitly requested.

## Layout And Spacing

- Build clear structure: aligned grids, predictable sections, readable content width, and consistent padding.
- Keep spacing generous enough to feel calm, but compact enough for operational interfaces such as dashboards and admin panels.
- Group related content with panels, cards, sections, or toolbars only when grouping improves scanning.
- Keep primary actions obvious and secondary actions quieter.
- Make layouts responsive by default: desktop, tablet, and mobile for web; safe areas and keyboard behavior for mobile; resizable panels for desktop.
- Avoid cramped screens, misaligned elements, tiny click targets, accidental overflow, and layout jumps.

## Shape, Depth, And Motion

- Use consistent rounded corners based on the existing design system. If none exists, prefer softly rounded controls and panels without making every element pill-shaped.
- Use subtle depth: soft shadows, low-contrast borders, and layered dark surfaces.
- Use glass or blur effects only when readability remains strong.
- Keep interaction motion smooth and purposeful: hover fades, button press feedback, modal transitions, sidebar movement, skeleton loading, and message streaming.
- Avoid excessive bouncing, long animations, glossy effects, and decoration that distracts from the task.

## Components

Buttons:
- Primary buttons use the accent color and clear text.
- Secondary buttons use dark surfaces with subtle borders.
- Ghost buttons stay quiet but must have visible hover, pressed, focused, and disabled states.
- Buttons must be large enough for mouse and touch use.

Inputs:
- Inputs use dark surfaces, readable text, clear labels, subtle borders, comfortable height, and visible focus states.
- Placeholder text is muted; validation errors are specific and recoverable.

Cards and panels:
- Cards group related content, use enough padding, and avoid unnecessary decoration.
- Do not nest decorative cards inside other decorative cards unless the project pattern already requires it.

Modals:
- Use a dimmed backdrop, clear title, concise content, natural close behavior, and one dominant action.
- Use centered dialogs on desktop and bottom-sheet patterns where appropriate on mobile.

Navigation:
- Keep navigation simple and predictable.
- Use clear active states, compact icons with labels where useful, and consistent sidebar, topbar, or bottom navigation patterns.

Tables and dashboards:
- Use comfortable row height, subtle separators, sticky or visible headers when useful, and top-level search/filter/sort controls when they improve the workflow.
- Metric cards should include a label, value, optional trend, optional icon, and restrained surface treatment.
- Avoid dense enterprise clutter.

Forms:
- Group fields logically, label inputs clearly, show validation near the problem, include loading and disabled states, and make submission status explicit.
- Break long forms into sections or steps when it improves completion.

Chat and AI interfaces:
- Use a calm dark background, readable message layout, visually distinct user messages, comfortable assistant response typography, and an accessible fixed or easy-to-reach composer.
- Keep actions such as copy, regenerate, edit, attach, voice, and image subtle but discoverable.
- Include useful empty, streaming, loading, retry, and error states.

Landing pages:
- Use a strong first viewport with a clear headline, concise support text, one primary call to action, optional secondary action, and premium dark visual depth.
- Use feature cards, screenshots, pricing, FAQ, and footer sections only when they serve the page goal.
- Avoid fake claims, flashy startup clutter, and generic filler content.

Widgets:
- Keep widgets compact, readable, adaptive, and free of text overflow.
- Preserve customization when relevant and keep controls visible without becoming bulky.

## Required States

Design important states before considering the UI complete:

- default
- hover
- pressed
- focused
- disabled
- loading
- empty
- error
- success

Use skeletons, subtle spinners, or progress indicators for loading. Empty states should explain what is missing and offer one useful action when appropriate. Error states should say what happened, how to recover, and provide retry or corrective action when possible.

## Accessibility And Quality Bar

- Keep text contrast readable and do not rely only on color for status.
- Use semantic HTML for web and meaningful labels for controls.
- Ensure keyboard-friendly interactions where the platform supports them.
- Prevent text overflow, overlapping elements, broken scrolling, and unstable layout.
- Make the UI work at more than one screen size unless the task explicitly asks for a fixed prototype.
- Keep implementation maintainable: reuse existing components, avoid duplicated UI logic, and do not add dependencies just for styling unless clearly justified.

## Final Check

Before finishing UI work, verify:

- The interface looks modern, premium, and complete.
- Spacing, alignment, colors, typography, and component states are consistent.
- Primary and secondary actions are clear.
- Responsive behavior is handled.
- Empty, loading, error, and success states are considered.
- The result does not look like a default framework template.
