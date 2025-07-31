# 1-2 Anki Add-ons

- [AnkiConnect (2055492159)](https://ankiweb.net/shared/info/2055492159)
- [Local Audio Server for Yomichan (1045800357)](https://ankiweb.net/shared/info/1045800357)
- [PassFail 2 Remove the Easy and Hard buttons (876946123)](https://ankiweb.net/shared/info/876946123)

Tools → Add-ons → Get Add-ons → Code:

```
2055492159 1045800357 876946123
```

## Local Audio Server

- Download the required audio files

- Run the following commands, depending on the language of the audio files:
  - Japanese

    ```bash
    tar -xf ~/Downloads/local-yomichan-audio-collection-*-opus.tar.xz -C ~/Downloads
    cp -rf ~/Downloads/user_files ~/.local/share/Anki2/addons21/1045800357
    rm -rf ~/Downloads/{local-yomichan-audio-collection-*-opus.tar.xz,user_files}
    ```

  - English

    ```bash
    unzip -qq ~/Downloads/Forvo_pronunciation/export/opus/en.zip -d ~/Downloads
    mv ~/Downloads/en ~/Downloads/forvo_files
    cp -rf ~/Downloads/forvo_files ~/.local/share/Anki2/addons21/1045800357/user_files
    rm -rf ~/Downloads/{Forvo_pronunciation,forvo_files}
    ```
