# Scrolling Text

An Android app that displays a long article about the *Beatles Anthology Vol. 1* in a scrollable two-column layout: a narrow left column for the subtitle and a wider right column for the article text. At the bottom of the article there is a button that shows a "Comment submitted!" message.

## Screenshots

| Top of the article | Scrolled down | After clicking the button |
|:---:|:---:|:---:|
| ![Top of the article](screenshots/screenshot1.png) | ![Scrolled down](screenshots/screenshot2.png) | ![Toast message](screenshots/screenshot3.png) |

## Features

- Title bar with the article heading
- Two-column layout: subtitle on the left (100dp wide), article text on the right
- The whole article scrolls vertically
- Clickable web link in the article text
- "Add comment" button at the end of the article that shows a Toast message

## What I used

**Language and tools**
- Java
- Android Studio
- XML for the layout and string resources

**Layouts and views**
- `ConstraintLayout` – root layout, positions the title and the scroll view with constraints
- `ScrollView` – makes the content scrollable (contains exactly one direct child)
- `LinearLayout` (vertical) – the single child of the ScrollView, stacks the columns and the button
- `LinearLayout` (horizontal) – places the subtitle and article side by side
- `TextView` – for the title, subtitle and article text
- `Button` – the "Add comment" button
- `Toast` – shows the "Comment submitted!" message when the button is clicked

## Project structure

```
app/src/main/
├── java/.../MainActivity.java      → button click listener and Toast
└── res/
    ├── layout/activity_main.xml    → the layout
    └── values/strings.xml          → all texts
```

---
*Adapted from Android Developer Fundamentals – Homework 1.3*
