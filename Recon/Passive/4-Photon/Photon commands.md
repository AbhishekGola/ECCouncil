Certainly! Below is a guide on using the Photon tool in cybersecurity, formatted in Markdown. Photon is a fast crawler designed for OSINT (Open Source Intelligence) purposes.

```markdown
# Photon Tool in Cybersecurity: Command Line Usage Guide

Photon is a fast web crawler designed for OSINT, making it useful in cybersecurity for gathering information about a target website.

## Installation

Photon requires Python 3.6 or higher. You can install it using `pip`.

1. **Clone the repository**:
    ```sh
    git clone https://github.com/s0md3v/Photon.git
    ```

2. **Navigate to the directory**:
    ```sh
    cd Photon
    ```

3. **Install the dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

## Basic Usage

Photon's basic syntax is:
```sh
python photon.py -u <URL> [options]
```

### Example
```sh
python photon.py -u https://example.com
```

This command will start crawling `https://example.com`.

## Command Line Options

Photon supports various options to customize its behavior.

### Basic Options

- `-u <URL>`: Specifies the target URL.
- `-l <LEVEL>`: Sets the level of depth to crawl. Default is 2.
- `-t <TIMEOUT>`: Sets the connection timeout in seconds. Default is 6.
- `-d <DIRECTORY>`: Specifies the directory to save the results. Default is `output`.

### Example
```sh
python photon.py -u https://example.com -l 3 -t 10 -d ~/output
```

This command crawls `https://example.com` with a depth of 3, a timeout of 10 seconds, and saves results to the `~/output` directory.

### Advanced Options

- `--wayback`: Use Wayback Machine snapshots to find URLs.
- `--keys`: Extract API keys.
- `--dns`: Perform DNS enumeration.
- `--export`: Export the data in JSON format.
- `--stdout`: Print the output to the terminal.

### Example
```sh
python photon.py -u https://example.com --wayback --keys --dns --export
```

This command performs a comprehensive crawl including Wayback Machine snapshots, API key extraction, DNS enumeration, and exports the results in JSON format.

### Rate Limiting

To avoid overloading the target server, use the `-r` option to set a rate limit:
```sh
python photon.py -u https://example.com -r 2
```
This sets a delay of 2 seconds between requests.

### User Agent

Photon allows you to specify a custom User Agent using the `-a` option:
```sh
python photon.py -u https://example.com -a "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36"
```

### HTTP Headers

You can include additional HTTP headers with the `-H` option:
```sh
python photon.py -u https://example.com -H "Authorization: Bearer <token>"
```

## Saving and Viewing Results

By default, Photon saves results in the `output` directory. You can specify a different directory using the `-d` option. Results are saved in multiple formats including text and JSON, depending on the options used.

### Viewing JSON Results
To view JSON results, you can use tools like `jq`:
```sh
cat ~/output/example_com.json | jq .
```

## Tips

- **Automate Tasks**: Combine Photon with other tools in scripts for automated information gathering.
- **Respect Robots.txt**: Although Photon allows ignoring `robots.txt`, it's good practice to respect it to avoid overloading servers.

## Further Reading

For more detailed information and advanced usage, refer to the [Photon GitHub Repository](https://github.com/s0md3v/Photon).

```

This guide provides a comprehensive overview of installing and using Photon for cybersecurity purposes, including basic and advanced command line options, tips, and further reading references.