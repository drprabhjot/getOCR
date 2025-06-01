# getOCR

### Repository Note
**Please be aware that this repository appears to be incomplete.** The `getOCR_Code` and `Use Case Example` files, which are referenced in the instructions, are not currently included. This may affect your ability to directly follow all steps as described. You may need to create these scripts based on the project description or obtain them from an alternative source.

This script leverages Google OCR technology to extract text from images, PDFs, and other files found on websites. The process involves:
1. Fetching the file from a specified URL.
2. Storing it as a Google Document in a designated Google Drive folder.
3. Reading the document content and returning it as text within a Google Script.

To optimize for frequent daily use, such as in web scraping, the script includes a feature to search Google Drive for an existing file by name before attempting to download it from the source URL. This minimizes redundant downloads and helps prevent potential IP blocks from websites due to excessive requests.

### Dependencies
*   A Google Script environment.
*   The "Drive API" must be enabled in your Google Advanced Services. (This is also mentioned in Step 1 of the setup, but reiterated here for clarity).

### Setup and Usage
Follow these steps to configure and use the script:

*   **Step 1:** Enable the Drive API.
    *   In your Google Script project, navigate to "Services" (or "Resources" > "Advanced Google services" in the legacy editor).
    *   Locate "Drive API" and toggle it to ON.
    *   If you rename the "Drive" service in your script, ensure you update the code accordingly.

*   **Step 2:** Add the OCR Script.
    *   You will need to obtain or create the `getOCR_Code` script and paste it into your Google Script editor. This file is not currently included in this repository.

*   **Step 3:** Prepare your Google Drive Folder.
    *   It's recommended to create a new folder in your Google Drive to store the files processed by this script.
    *   Obtain the Folder ID from the folder's URL. For example, if the URL is `https://drive.google.com/drive/u/0/folders/1dTMIT-8haAWLZ1JF1_tAGtBHdULAQ`, the Folder ID is `1dTMIT-8haAWLZ1JF1_tAGtBHdULAQ`.

*   **Step 4:** Identify the File URL.
    *   Get the direct URL of the file (e.g., image, PDF) you want to process from the source website. This is the URL of the file itself, not the webpage it's embedded on.

*   **Step 5:** Define a Unique Filename.
    *   Choose a name for how the file will be saved in your Google Drive folder.
    *   **Crucially, ensure this filename is unique for each new file you process.** For instance, append the current date or a timestamp if files are published daily or less frequently. The script checks for this filename in Google Drive; if a file with the same name already exists, it will *not* fetch the new file from the provided URL.

*   **Step 6:** Implement Your Use Case.
    *   Refer to your `Use Case Example` script for a sample of how to retrieve and use the transcribed text. This file is not currently included in this repository, so you may need to create it based on the project's description.
