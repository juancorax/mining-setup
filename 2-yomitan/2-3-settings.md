# 2-3 Yomitan Settings

## Shared Settings

### Advanced: ✅

### Scanning

- Scan delay (in milliseconds): `0`

### Popup Behavior

- Allow scanning popup content: ✅
  - Maximum number of child popups: `5`

### Appearance

- Theme
  - Shadow: Light

- Font size: `20`

- Configure custom CSS
  - Popup CSS:

    ```css
    .definition-item {
      --collapsible-definition-line-count: 1;
    }
    ```

### Popup Position & Size

- Scale: 125%
  - Auto-scale
    - Zoom level: ✅

- Size
  - Width: `700`

  - Height: `350`

### Anki

- Enable Anki integration: ✅

## Profiles

### Profile

- Configure profiles…

  |     | Default | Name     | Conditions                              |
  | --- | ------- | -------- | --------------------------------------- |
  | 1   | ✅      | Japanese | 0                                       |
  | 2   | ❌      | English  | 1 → if `Modifier Keys` `Include` `Ctrl` |

## Japanese Profile

### Appearance

- Font family:

  ```
  "DejaVuSansM Nerd Font Mono", "Noto Serif CJK JP", "IPAexMincho", "Jigmo", "Jigmo2", "Jigmo3"
  ```

### Audio

- Configure audio playback sources…
  - Custom URL (JSON)
    - URL:

      ```
      http://127.0.0.1:5050/?term={term}&reading={reading}
      ```

### Translation

- Configure custom text replacement patterns…

  | Pattern                 | Replacement |
  | ----------------------- | ----------- |
  | `1\|１`                 | `一`        |
  | `2\|２`                 | `二`        |
  | `3\|３`                 | `三`        |
  | `4\|４`                 | `四`        |
  | `5\|５`                 | `五`        |
  | `6\|６`                 | `六`        |
  | `7\|７`                 | `七`        |
  | `8\|８`                 | `八`        |
  | `9\|９`                 | `九`        |
  | `・\|、\|\-\|\.\|‐\|\s` |             |
  | `ッ`                    | `っ`        |
  | `(.)々`                 | `$1$1`      |

### Anki

- Configure Anki flashcards…
  - Expression/Reading

    Deck/Model: Japanese Mining

    | Field       | Value                    |
    | ----------- | ------------------------ |
    | Expression  | `{expression}`           |
    | Sentence    | `{sentence}`             |
    | Reading     | `{reading}`              |
    | PitchAccent | `{pitch-accents}`        |
    | Glossary    | `{popup-selection-text}` |
    | Audio       | `{audio}`                |

## English Profile

### General

- Language: English (en)

### Appearance

- Font family:

  ```
  "DejaVuSansM Nerd Font Mono"
  ```

### Audio

- Configure audio playback sources…
  - Custom URL (JSON)
    - URL:

      ```
      http://127.0.0.1:5050/?term={term}
      ```

### Anki

- Configure Anki flashcards…
  - Expression

    Deck/Model: English Mining

    | Field      | Value                    |
    | ---------- | ------------------------ |
    | Expression | `{expression}`           |
    | Sentence   | `{sentence}`             |
    | Glossary   | `{popup-selection-text}` |
    | Audio      | `{audio}`                |
