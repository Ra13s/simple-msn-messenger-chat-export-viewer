# Simple MSN Messenger Chat Export Viewer

A simple, client-side HTML viewer for legacy MSN Messenger / Windows Live Messenger XML log files (`.xml`).

This tool allows you to browse your exported Messenger conversations **locally** in your web browser without needing to upload your sensitive chat data anywhere.

## Features

*   **Local Processing:** Your `.xml` log files are processed entirely within your browser using JavaScript. **No data is uploaded or sent anywhere.** This is crucial for protecting the privacy of your chat history.
*   **Conversation Grouping:** Displays conversations grouped by the chat partner's name (derived from the log filenames).
*   **Message Display:** Shows messages chronologically within a selected conversation.
    *   Highlights *your* messages once you identify your display name(s).
    *   Displays sender names (FriendlyName) and timestamps.
    *   Renders basic inline formatting found in the logs (e.g., color, bold, italic, underline).
    *   Detects and creates clickable links for URLs in messages.
    *   Shows separators between different chat sessions within the same file.
*   **Identify Yourself:** Allows you to select your own display name(s) from those found in the logs, making it easy to distinguish your messages visually. You can set multiple names if yours changed over time and unset them if needed.
*   **Simple Interface:** Basic, clean interface focused on readability.
*   **Multi-File Support:** Can load and process multiple `.xml` log files at once.

## How to Use

1.  **Download:** Get the `index.html` file.
2.  **Find Your Logs:** Locate your old MSN Messenger / Windows Live Messenger chat logs. These are typically `.xml` files stored in folders like `My Documents\My Received Files\<YourEmail>\History` or similar paths within your user profile from older Windows versions.
3.  **Open:** Open the `index.html` file in your modern web browser (Firefox, Chrome, Edge, Safari etc.).
4.  **Select File(s):** Click the "Select Log File(s)" button. Choose one or more `.xml` log files you found in step 2. Use Ctrl+Click (or Cmd+Click on Mac) or Shift+Click to select multiple files in the dialog. **Note:** Your files are processed directly in your browser and are *never* uploaded.
5.  **Browse:**
    *   Your conversations (grouped by filename) will load in the sidebar.
    *   Click on a conversation name to view its messages.
    *   Use the "Identify Yourself" section in the sidebar: click "Set as Me" next to the display name(s) you used to highlight your messages. Click "Unset Me" if you make a mistake.

## GitHub Pages (Live Demo)

You can use a live version of this tool hosted directly via GitHub Pages at the following URL:

**[https://Ra13s.github.io/simple-msn-messenger-chat-export-viewer/](https://Ra13s.github.io/simple-msn-messenger-chat-export-viewer/)**

Using the live version **still processes your files locally** in *your* browser – your chat data is not sent to the server hosting the page.

## Privacy

Your privacy is paramount, especially concerning personal chat logs. This tool is designed to work completely offline or with local browser processing only. Your chat data remains on your computer and is **never transmitted over the internet** by this tool. All processing happens locally in your web browser.

## Limitations

*   **Performance:** Loading a very large number of log files, or individual files containing tens of thousands of messages, might cause the browser to become slow or unresponsive during processing.
*   **Formatting:** Only renders basic inline styles (color, font-weight, font-style, text-decoration) specified in the `<Text Style="...">` attribute. Does **not** render custom emoticons, winks, nudges, background images, or other non-textual elements.
*   **Media/Files:** Does **not** display images, file transfers, display pictures, or any media content. Only the text of the chat is shown.
*   **Conversation Grouping:** Relies solely on filenames to group conversations. If multiple distinct chats were logged to files with the same base name (e.g., "JohnDoe.xml", "JohnDoe1.xml"), they will appear as one conversation entry in the list.
*   **Error Handling:** Basic error handling for XML parsing is included, but severely corrupted or non-standard `.xml` log files might cause issues or fail to load.

## Development Note

This tool was developed mostly with assistance from AI models.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file (if included) or refer to the standard MIT License text.