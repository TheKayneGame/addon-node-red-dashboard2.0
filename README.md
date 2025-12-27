# Home Assistant Node-RED Dashboard addon

Gain access to the Node-RED dashboard 2.0 from Home Assistant sidebar

> No need to open Node-RED 2.0 webview port

## Detailed installation instructions

### Add the custom repository

Click the following button:

[![Add repository][badge-img]][badge-link]

[badge-img]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[badge-link]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FTheKayneGame%2Faddon-node-red-dashboard2.0

Or:

1. Navigate in your Home Assistant frontend to <kbd>Configuration</kbd> ->
   <kbd>Add-ons, Backups & Supervisor</kbd>
   -> <kbd>Add-ons</kbd> -> <kbd>ADD-ON STORE</kbd>.

1. Click the 3-dots menu at upper right <kbd>...</kbd> > <kbd>Repositories</kbd>
   and add this repository's URL
   [https://github.com/TheKayneGame/addon-node-red-dashboard2.0](https://github.com/TheKayneGame/addon-node-red-dashboard2.0)
   :

  <img src="images/add_ss.png" width="300"/>

### Install the addon

1. Scroll down the page to find the new repository, and click
   the new add-on named "Node-RED Dashboard 2.0"

   <img src="images/repo_ss.png" width="429"/>

1. Click <kbd>Install</kbd> and give it a few minutes to finish downloading.

1. Click <kbd>Start</kbd>, give it a few seconds to spin up, and
   then click the <kbd>Open Web UI</kbd> button that appears.

## CI notes

- The GitHub Actions CI intentionally skips the `frenck/action-addon-linter` step on hosted runners due to Docker build compatibility issues observed in the action.
- To run the addon linter:
    - Run it locally.
    - Use a self-hosted runner that has Docker available.

- The CI was updated to:
    - Fix MD013 by converting long badge URLs to reference-style links.
    - Run Prettier via Node.js (setup + npm ci + npx prettier) to avoid the "prettier: command not found" error.

If you want, I can add a CONTRIBUTING or CI document with exact commands to run the linter locally or the recommended self-hosted runner setup.
