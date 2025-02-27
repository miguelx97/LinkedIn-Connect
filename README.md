# LinkedIn Auto Connect

## Overview

This Tampermonkey script automates the process of sending connection requests on LinkedIn. It adds an "Auto Connect" button to the My Network page, which, when clicked, automatically sends requests to users with a specified number of mutual connections.

## Features

- Adds an "Auto Connect" button to LinkedIn's My Network page.
- Automatically scrolls to load more connection suggestions.
- Highlights profiles based on mutual connections.
- Sends connection requests only to users with a minimum number of mutual connections.
- Stops after a set number of requests to prevent LinkedIn restrictions.

## Installation

1. Install the [Tampermonkey extension](https://www.tampermonkey.net/) for your browser.
2. Click the Tampermonkey icon and select "Create a new script".
3. Delete the default template and paste the script.
4. Make sure CONFIG.DEV_MODE is set to false
5. Save the script and enable it.
6. Open [LinkedIn My Network](https://www.linkedin.com/mynetwork/grow/) and click the "Auto Connect" button.

## Usage

1. Navigate to [LinkedIn My Network](https://www.linkedin.com/mynetwork/grow/).
2. Click the **Auto Connect** button in the top bar (If the button does not appear, refresh the page).
3. The script will scroll through the page, highlight users, and send connection requests.
4. The process stops after reaching the defined connection limit.

## Configuration

Modify these variables in the script to customize behavior:

```javascript
const numMutualConnToConnect = 20; // Minimum mutual connections required
const limitConnections = 10; // Maximum number of connection requests per run
const limitScroll = 8; // Number of scroll actions to load users
```

## Troubleshooting

- Ensure the Tampermonkey extension is enabled.
- If the button does not appear, refresh the page.
- LinkedIn UI updates may break the script. If so, update the DOM selectors accordingly.

## Disclaimer

Use this script responsibly. Excessive automated actions may result in LinkedIn restrictions or account suspension.

## License

This project is licensed under the MIT License.
