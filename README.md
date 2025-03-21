# Proxer Releases

> [!IMPORTANT]
> Please note that the open-source version of the proxy client has been moved to [`proxer-cli`](https://github.com/doroved/proxer-cli).

> **Subscribe to us on [Telegram](https://t.me/macproxer) to receive notifications about new versions and updates.**

Proxying TCP traffic on macOS with domain filtering via UI

![proxer screenshot](proxer.png)

The current repository is intended for storing releases of the commercial version of Proxer as a macOS application.

Currently, an alpha version has been released for users who need access to YouTube and Discord through our paid proxy.

Subsequent development will implement all the functionality of `proxer-cli` + new features/improvements and will be free until the stable version is released.

The payment model for using Proxer with both your proxies and ours is under development.

## Installation

Currently, installation/update occurs by running `install.sh` from the command line.

In the future, releases will be signed with a certificate, and you will be able to download the application directly.

```bash
curl -fsSL https://raw.githubusercontent.com/doroved/proxer/main/install.sh | bash
```

## How to run with logging enabled

```bash
/Applications/proxer.app/Contents/MacOS/proxer
```

## How to check the proxy server's functionality

Run this command in the terminal, before that, make sure Proxer is running:

```bash
curl -I -v -x http://127.0.0.1:9999 https://www.youtube.com
```

If you receive a response with code `200`, everything is fine; if not, there is a problem with the connection to the proxy server. Please [message me](https://t.me/doroved) on Telegram, and I will try to resolve this issue.

## I have `Ping > 0`, but YouTube is not working

If you see `Ping > 0`, but YouTube is not opening, you need to disable `VPN/Proxy` service extensions in your browser.
