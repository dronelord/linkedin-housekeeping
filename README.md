# LinkedIn Comment Deleter

A browser-based script to automatically delete your LinkedIn comments. This script helps you bulk delete comments you've made on LinkedIn posts, saving you from having to manually delete them one by one.

## Features

- Automatically finds and deletes your comments on LinkedIn
- Handles pagination by clicking "Show more" buttons and scrolling
- Continues until all comments are deleted
- Includes error handling and retry mechanisms
- Provides console logging for progress tracking
- Can be stopped manually at any time

## Prerequisites

Before you begin, ensure you have:
- A modern web browser (Chrome, Firefox, Edge, etc.)
- Access to your browser's developer console
- Logged into LinkedIn in your browser

## Installation

1. Copy the entire content of `comment-deleter.js`
2. Navigate to your LinkedIn profile or activity page where your comments are visible
3. Open your browser's developer console:
   - Chrome/Edge: Press `F12` or `Ctrl + Shift + J` (Windows/Linux) or `Cmd + Option + J` (Mac)
   - Firefox: Press `F12` or `Ctrl + Shift + K` (Windows/Linux) or `Cmd + Option + K` (Mac)

## Usage

1. Once you're on the LinkedIn page with your comments:

```javascript
// 1. Open your browser's developer console
// 2. Paste the entire script content
// 3. Press Enter to start the deletion process
```

2. The script will automatically:
   - Find comment dropdown buttons
   - Click the delete option
   - Confirm deletion
   - Load more comments when available
   - Continue until all comments are processed

3. To stop the script at any time:
```javascript
stopCommentDeletion()
```

## Console Output

The script provides detailed console logging to help you track its progress:
```
*** Starting comment deletion process ***
Scanning for comment dropdowns...
Found 5 comment dropdown buttons
Clicking dropdown button...
Found delete option, clicking...
Successfully deleted comment
...
```

## Troubleshooting

If you encounter issues:

1. **Script not finding comments:**
   - Make sure you're on a page where your comments are visible
   - Try scrolling manually to load some comments before running the script
   - Check if the comments are actually visible in the UI

2. **Script not stopping:**
   - Use the `stopCommentDeletion()` command in the console
   - Refresh the page to completely stop the script

3. **Script throwing errors:**
   - Check if you're logged into LinkedIn
   - Ensure you have a stable internet connection
   - Try refreshing the page and running the script again

## Known Limitations

- The script can only delete comments you have permission to delete
- LinkedIn's UI updates may require script updates
- Rate limiting by LinkedIn may slow down the deletion process
- Very long comment histories may require multiple runs

## Technical Details

The script works by:
1. Finding comment dropdown buttons using LinkedIn's CSS classes
2. Simulating clicks on the delete options
3. Confirming deletions through modal dialogs
4. Handling pagination through scrolling and "Show more" buttons
5. Using promises and async/await for reliable timing

## Contributing

Feel free to submit issues and enhancement requests! To contribute:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Disclaimer

This script is provided as-is without any guarantees. Always review the code before running scripts in your browser console. Use at your own risk and ensure you want to delete the comments before running the script.

## License

This project is licensed - see the LICENSE file for details.
