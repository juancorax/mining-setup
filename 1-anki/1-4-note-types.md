# 1-4 Anki Note Types

Tools → Manage Note Types (Ctrl + Shift + n)

## Add

- Add → Add: Basic
  - Name: `Japanese Mining` or `English Mining`

## Japanese Note Type

### Fields

- Select note type → Fields

  | Position | Field         |
  | :------: | ------------- |
  |    1     | `Expression`  |
  |    2     | `Hint`        |
  |    3     | `Reading`     |
  |    4     | `PitchAccent` |
  |    5     | `Glossary`    |
  |    6     | `Picture`     |
  |    7     | `Sentence`    |
  |    8     | `Audio`       |

### Cards

- Select note type → Cards
  - Front Template

    ```html
    <span lang="ja">
      <div id="expression">{{Expression}}</div>
      <div>{{Hint}}</div>
    </span>
    ```

  - Back Template

    ```html
    {{FrontSide}}

    <hr />

    <span lang="ja">
      <div id="reading">{{Reading}}</div>
      <div>{{PitchAccent}}</div>
      <div id="glossary">{{Glossary}}</div>
      <div>{{Picture}}</div>
      <div>{{Sentence}}</div>
      <div id="audio">{{Audio}}</div>
    </span>
    ```

  - Styling

    ```css
    .card {
      max-width: 600px;
      margin: 0 auto;
      font-family:
        "DejaVuSansM Nerd Font Mono", "Noto Serif CJK JP", "IPAexMincho",
        "Jigmo", "Jigmo2", "Jigmo3";
      font-size: 25px;
      color: #c5c9c5 !important;
      background-color: #181616 !important;
    }

    .card div {
      margin: 25px 0;
    }

    #expression,
    #reading {
      font-size: 50px;
    }

    #glossary li {
      margin: 12.5px 0;
    }

    #audio {
      display: none;
    }

    img {
      width: auto;
      height: auto;
    }
    ```

## English Note Type

### Fields

- Select note type → Fields

  | Position | Field        |
  | :------: | ------------ |
  |    1     | `Expression` |
  |    2     | `Sentence`   |
  |    3     | `Glossary`   |
  |    4     | `Picture`    |
  |    5     | `Audio`      |

### Cards

- Select note type → Cards
  - Front Template

    ```html
    <div id="expression">{{Expression}}</div>
    <div id="sentence">{{Sentence}}</div>
    ```

  - Back Template

    ```html
    {{FrontSide}}

    <hr />

    <div id="glossary">{{Glossary}}</div>
    <div>{{Picture}}</div>
    <div id="audio">{{Audio}}</div>
    ```

  - Styling

    ```css
    .card {
      max-width: 600px;
      margin: 0 auto;
      font-family: "DejaVuSansM Nerd Font Mono";
      font-size: 20px;
      color: #c5c9c5 !important;
      background-color: #181616 !important;
    }

    .card div {
      margin: 20px 0;
    }

    #expression {
      font-size: 40px;
    }

    #sentence {
      color: #a6a69c;
    }

    #glossary li {
      margin: 10px 0;
    }

    #audio {
      display: none;
    }

    img {
      width: auto;
      height: auto;
    }
    ```
