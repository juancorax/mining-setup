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
  |    2     | `Sentence`    |
  |    3     | `Reading`     |
  |    4     | `PitchAccent` |
  |    5     | `Glossary`    |
  |    6     | `Picture`     |
  |    7     | `Audio`       |

### Cards

- Select note type → Cards
  - Front Template

    ```html
    <span lang="ja">
      <div id="expression">{{Expression}}</div>
      <div id="sentence">{{Sentence}}</div>
    </span>
    ```

  - Back Template

    ```html
    {{FrontSide}}

    <hr />

    <span lang="ja">
      <div id="reading">{{Reading}}</div>
      <div id="pitch-accent">{{PitchAccent}}</div>
      <div id="glossary">{{Glossary}}</div>
    </span>

    <div>{{Picture}}</div>
    <div id="audio">{{Audio}}</div>

    <script>
      if (
        document.getElementById("reading").textContent ==
        document.getElementById("expression").textContent
      ) {
        document.getElementById("reading").remove();
      }

      document.getElementById("pitch-accent").innerHTML = document
        .getElementById("pitch-accent")
        .innerHTML.replace(/<\/?ol>|<\/?li>/g, "")
        .trim();
    </script>
    ```

  - Styling

    ```css
    .card {
      max-width: 600px;
      margin: 0 auto;
      font-family:
        "Noto Serif CJK JP", "IPAexMincho", "Jigmo", "Jigmo2", "Jigmo3";
      font-size: 20px;
      color: #c5c9c5 !important;
      background-color: #181616 !important;
    }

    .card div {
      margin: 20px 0;
    }

    #expression,
    #reading {
      font-size: 40px;
      font-weight: bold;
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

    hr {
      border-color: #c8c093;
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
      font-weight: bold;
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

    hr {
      border-color: #c8c093;
    }

    img {
      width: auto;
      height: auto;
    }
    ```
