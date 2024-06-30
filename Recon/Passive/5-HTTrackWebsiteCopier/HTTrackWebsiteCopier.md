Certainly! Below is a guide on how to use "HTTrack Website Copier" written in Markdown format:

```markdown
# HTTrack Website Copier Usage Guide

HTTrack is a free and open-source tool for downloading websites to your local directory. It allows you to download a World Wide Web site from the Internet to a local directory, building all directories recursively, getting HTML, images, and other files from the server to your computer.

## Installation

### Windows
1. Download the installer from the [HTTrack Website](https://www.httrack.com/page/2/en/index.html).
2. Run the installer and follow the on-screen instructions.

### macOS
1. Install Homebrew if you don't have it already:
    ```sh
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
2. Install HTTrack using Homebrew:
    ```sh
    brew install httrack
    ```

### Linux
1. For Debian-based distributions (like Ubuntu):
    ```sh
    sudo apt-get install httrack
    ```
2. For Red Hat-based distributions (like Fedora):
    ```sh
    sudo dnf install httrack
    ```

## Basic Usage

1. **Open HTTrack**:
   - On Windows, launch HTTrack from the Start menu.
   - On macOS and Linux, you can use the terminal.

2. **Create a New Project**:
   - Enter a project name.
   - Select the base path where the downloaded files will be saved.

3. **Enter the URLs**:
   - Add the URL(s) of the website you want to download.

4. **Set Preferences** (optional):
   - You can set options like maximum depth, download speed, and file types to include/exclude.

5. **Start the Download**:
   - Click "Next" and then "Finish" to start the download process.

## Command Line Usage

For more advanced users, HTTrack can be used directly from the command line.

### Basic Command

```sh
httrack "http://example.com" -O "/path/to/destination/directory"
```

### Options

- `-O` : Specifies the output directory.
- `-r` : Sets the maximum recursion depth.
- `-%v` : Enables verbose mode.
- `-A1000000` : Sets the maximum transfer rate in bytes per second.

### Example

```sh
httrack "http://example.com" -O "~/mywebsite" -r3 -%v
```

This command downloads the website at `http://example.com` to the `~/mywebsite` directory with a recursion depth of 3 and verbose output.

## Tips

- **Updating a Mirror**: To update an existing mirror, run the same command again. HTTrack will update the downloaded files to match the website.
- **Ignoring Robots.txt**: Use the `-s0` option to ignore the `robots.txt` file (not recommended for most uses).
- **Proxy Settings**: If you need to use a proxy, you can set it with the `--proxy` option:
    ```sh
    httrack "http://example.com" -O "~/mywebsite" --proxy "http://proxyserver:port"
    ```

## Further Reading

For a complete list of options and detailed documentation, visit the [HTTrack documentation](https://www.httrack.com/html/fcguide.html).

```

This guide provides a comprehensive overview of installing and using HTTrack, both through its graphical interface and the command line, along with useful tips and further reading references.