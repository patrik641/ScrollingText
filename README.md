# Scrolling Text

An Android app that displays a long article about the *Beatles Anthology Vol. 1* in a scrollable two-column layout: a narrow left column for the subtitle and a wider right column for the article text. At the bottom of the article there is a button that shows a "Comment submitted!" message.

## Screenshots

| Top of the article | Scrolled down | After clicking the button |
|:---:|:---:|:---:|
| <img width="250" alt="Top of the article" src="https://github.com/user-attachments/assets/9a3a154c-44c5-4efd-b42a-f4797e369226" /> | <img width="250" alt="Scrolled down" src="https://github.com/user-attachments/assets/c414fbbf-167b-4ef0-a5d4-0c0eb875f0a9" /> | <img width="250" alt="After clicking the button" src="https://github.com/user-attachments/assets/2370027b-a642-4f94-8aca-f7ced8668063" /> |

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
