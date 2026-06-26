# Clappia Daemon

A lightweight background service that connects the Clappia web application to your local printer hardware.

## Install

### macOS & Linux

```bash
curl -fsSL https://github.com/clappia-dev/clappia-daemon/releases/download/v1.0.0/install.sh | sh
```

This auto-detects your OS and architecture, downloads the correct binary, and sets everything up.

After install:

```bash
# Start
~/.clappia/clappia-daemon --port 1984 --daemon

# Stop
~/.clappia/clappia-daemon --stop
```

### macOS - Manual download

1. Download `clappia-daemon-darwin-<arch>.zip` from the [Releases](https://github.com/clappia-dev/clappia-daemon/releases) page.
2. Extract the `.app` bundle and move it to your `Applications` folder.
3. If macOS blocks it, open **Terminal** and run:

    ```bash
    xattr -dr com.apple.quarantine /Applications/Clappia\ Daemon.app
    ```

Then double-click the app to run it in the background.

### Linux - Manual download

1. Download `clappia-daemon-linux-<arch>.zip` from the [Releases](https://github.com/clappia-dev/clappia-daemon/releases) page.
2. Extract and make the binary executable:

    ```bash
    unzip clappia-daemon-linux-*.zip && chmod +x clappia-daemon
    ```

3. Run in the background:

    ```bash
    ./clappia-daemon --port 1984 --daemon
    ```

    To stop later:

    ```bash
    ./clappia-daemon --stop
    ```

### Windows

1. Download `clappia-daemon-windows-amd64.zip` from the [Releases](https://github.com/clappia-dev/clappia-daemon/releases) page.
2. Extract and run `clappia-daemon.exe`.

A helper script (`run.vbs`) is included to launch the daemon without a console window.
