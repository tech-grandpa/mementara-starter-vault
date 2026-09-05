# Diagrams and rich notes

## A simple flow

```mermaid
flowchart LR
  Write[Write Markdown] --> GitHub[Commit to GitHub]
  GitHub --> Download[Download snapshot]
  Download --> Read[Read offline]
```

## A conversation

```mermaid
sequenceDiagram
  Reader->>Notebook: Find a passage
  Notebook-->>Reader: Open the matching heading
```

## Math

Inline math: $E = mc^2$.

$$\sum_{k=1}^{n} k = \frac{n(n+1)}{2}$$

## Code

```swift
let message = "Your knowledge, within reach."
print(message)
```

## Table

| Feature | Offline |
| --- | --- |
| Downloaded notes | Yes |
| Search | Yes |
| Cached media | Yes |
| Remote images | No automatic requests |

- [x] Read the sample
- [ ] Create your own notebook

[[Welcome#^compass|Return to the compass passage]]

## Class diagram

```mermaid
classDiagram
  Vault "1" --> "many" Note
  Note : title
  Note : path
```

## Snapshot states

```mermaid
stateDiagram-v2
  [*] --> Downloading
  Downloading --> NotesReady
  NotesReady --> MediaReady
  MediaReady --> [*]
```

## Relationships

```mermaid
erDiagram
  VAULT ||--o{ NOTE : contains
  NOTE ||--o{ SECTION : indexes
```

## A small timeline

```mermaid
gantt
  title A notebook release
  dateFormat YYYY-MM-DD
  section Reader
  Write notes :2026-09-01, 2d
  Download and test :2026-09-03, 2d
```
