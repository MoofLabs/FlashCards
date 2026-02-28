# Flashcard Study

A simple, offline-first flashcard app built as a progressive web app (PWA). Made for studying on the go -- works without an internet connection once installed.

## What it does

- Create flashcard sets with text and images on either side
- Study cards with tap-to-flip, shuffle, and keyboard navigation
- Import and export sets as JSON or CSV for sharing between devices
- Rename, edit, and manage sets from the home screen
- Installs to your home screen on any device

## How to use

Open the app in a browser and tap "Add to Home Screen" (or the install prompt) to install it. Everything runs locally in your browser -- no accounts, no server, no tracking.

### Creating cards

1. Create a new set from the home screen
2. Tap Edit to open the set
3. Add cards with text, images, or both on the front and back
4. Tap Study Now when you're ready

### Keyboard shortcuts (study mode)

- **Space** -- flip the card
- **Left arrow** -- previous card
- **Right arrow** -- next card

### Importing cards

Supports two formats:

**JSON** -- the native export format. Importing a JSON file will merge cards into existing sets with the same name, or create new sets.

**CSV** -- a simple two-column format. The first column is the front of the card, the second is the back. A header row of `front,back` is optional and will be skipped. Quoted fields are supported.

```
front,back
What is the capital of France?,Paris
"Who wrote ""1984""?",George Orwell
```

## Hosting

This is a static site -- just serve the files from any web server or GitHub Pages. No build step required.

## Storage

All data lives in your browser's localStorage. Images are resized to 800px max and stored as base64. Keep in mind that localStorage has a ~5MB limit per origin, so heavy image use will fill up faster.
