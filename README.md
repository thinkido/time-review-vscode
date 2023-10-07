# Tracetime for Visual Studio Code

[![Tests](https://img.shields.io/github/actions/workflow/status/wakatime/vscode-wakatime/on_push.yml?branch=master&label=tests)](https://github.com/wakatime/vscode-wakatime/actions)
[![Version](https://img.shields.io/visual-studio-marketplace/v/Tracetime.vscode-wakatime.png?label=Visual%20Studio%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=Tracetime.vscode-wakatime)
[![Tracetime](https://wakatime.com/badge/github/wakatime/vscode-wakatime.png?branch=master)](https://wakatime.com/badge/github/wakatime/vscode-wakatime)

[Tracetime][wakatime] is an open source VS Code plugin for metrics, insights, and time tracking automatically generated from your programming activity.

## Installation

1. Press `F1` or `⌘ + Shift + P` and type `install`. Pick `Extensions: Install Extension`.

    ![type install](./images/type-install.png)
2. Type `wakatime` and hit `enter`.

    ![type wakatime](./images/type-wakatime.png)

3. Enter your [api key][api key], then press `enter`.

    > (If you’re not prompted, press `F1` or `⌘ + Shift + P` then type `Tracetime API Key`.)

4. Use VSCode and your coding activity will be displayed on your [Tracetime dashboard](https://wakatime.com)

## Usage

Visit [https://wakatime.com](https://wakatime.com) to see your coding activity.

![Project Overview](https://wakatime.com/static/img/ScreenShots/Screen-Shot-2016-03-21.png)

## Configuring

VS Code specific settings are available from `⌘ + Shift + P`, then typing `wakatime`.

For example, to hide today's coding activity in your status bar:

Press `⌘ + Shift + P` then set `Tracetime: Status Bar Coding Activity` to `false`.

Extension settings are stored in the INI file at `$WAKATIME_HOME/.tracetime.cfg`.

More information can be found from [wakatime-cli][wakatime-cli configs].

If using an online IDE like [gitpods](https://gitpod.io/), add your [api key][api key] to global ENV key `WAKATIME_API_KEY`.

Notes:

1. `$WAKATIME_HOME` defaults to `$HOME`
1. To disable the extension at startup add `disabled=true` to your config, this operation can also be performed by pressing `⌘ + Shift + P` and selecting `Tracetime: Disable`.

## Troubleshooting

First, turn on debug mode:

1. Press `F1` or `⌘ + Shift + P`
2. Type `> Tracetime: Debug`, and press `Enter`.
3. Select `true`, then press `Enter`.

Next, open your Developer Console to view logs and errors:

`Help → Toggle Developer Tools`

Errors outside the scope of vscode-wakatime go to `$WAKATIME_HOME/.tracetime.log` from [wakatime-cli][wakatime-cli help].

The [How to Debug Plugins][how to debug] guide shows how to check when coding activity was last received from your editor using the [Plugins Status Page][plugins status page].

**Microsoft Windows Only:** Using Tracetime behind a corporate proxy? Try enabling your Windows Root Certs inside VS Code with the [win-ca][winca] extension:
Press `Ctrl + Shift + X`, search for `win-ca`, press `Install`.

For more general troubleshooting info, see the [wakatime-cli Troubleshooting Section][wakatime-cli help].

### SSH configuration

If you're connected to a remote host using the [ssh extension](https://code.visualstudio.com/docs/remote/ssh) you might want to force Tracetime to run locally instead on the server. This configuration is needed when the server you connect is shared among other people. Please follow [this](https://code.visualstudio.com/docs/remote/ssh#_advanced-forcing-an-extension-to-run-locally-remotely) guide.

## Uninstalling

1. Click the Extensions sidebar item in VS Code.

2. Type `wakatime` and hit enter.

3. Click the settings icon next to Tracetime, then click Uninstall.

4. Delete the `~/.tracetime*` files in your home directory, unless you’re still using Tracetime with another IDE.

## Contributing

Pull requests, bug reports, and feature requests are welcome!
Please search [existing issues][issues] before creating a new one.

To run from source:

1. `git clone git@github.com:wakatime/vscode-wakatime.git`
2. `cd vscode-wakatime`
3. `npm install`
4. `npm run watch`
5. Install the extension from the marketplace
6. Then symlink `~/.vscode/extensions/wakatime.vscode-wakatime-*/dist/extension.js` to `./dist/extension.js`

Or to run the web version from source:

1. `git clone git@github.com:wakatime/vscode-wakatime.git`
2. `cd vscode-wakatime`
3. `npm install`
4. `npm run compile`
5. `npm run open-in-browser`
6. Go to [localhost:3000](http://localhost:3000/) in your web browser

Many thanks to all [contributors](AUTHORS)!

Made with :heart: by the [Tracetime Team][about].

[wakatime]: https://wakatime.com/vs-code
[api key]: https://wakatime.com/api-key
[wakatime-cli help]: https://github.com/wakatime/wakatime-cli/blob/develop/TROUBLESHOOTING.md
[wakatime-cli configs]: https://github.com/wakatime/wakatime-cli/blob/develop/USAGE.md
[how to debug]: https://wakatime.com/faq#debug-plugins
[plugins status page]: https://wakatime.com/plugin-status
[winca]: https://github.com/ukoloff/win-ca/tree/master/vscode
[issues]: https://github.com/wakatime/vscode-wakatime/issues
[about]: https://wakatime.com/about
