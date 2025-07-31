# 1-1 Anki Installation

## Requirements

- Run the following command:

  ```bash
  sudo apt install -y libnss3 libxcb-cursor0 libxcb-xinerama0 zstd
  ```

## Installing

- Download Anki from [here](https://github.com/ankitects/anki/releases/latest)

- Run the following commands:

  ```bash
  tar -xaf ~/Downloads/anki-launcher-*-linux.tar.zst -C ~/Downloads
  cd ~/Downloads/anki-launcher-*-linux
  sudo ./install.sh
  cd -
  rm -rf ~/Downloads/anki-launcher-*-linux*
  ```
