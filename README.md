# Email-extractor-from-social-url-
This script automates the process of scraping emails from Instagram bios using Selenium

🔹 How the Script Works
1️⃣ Set Up WebDriver & Load Environment Variables
Installs and configures Selenium with Chrome WebDriver.
Uses a .env file to securely store Instagram login credentials.
Reads Instagram profile URLs from an Excel file (urls.xlsx).
2️⃣ Log in to Instagram
Opens Instagram and waits for the login page to load.
Enters the stored username and password.
Clicks the login button and waits for authentication.
3️⃣ Visit Each Profile & Extract Emails
Goes to each Instagram profile URL.
Waits for the page to load fully.
Extracts the bio content using a CSS selector.
Uses a regular expression (regex) to find email addresses inside the bio.
4️⃣ Save Emails to an Excel File
Stores the extracted email along with the profile URL.
Saves progress to an Excel file (emails_extracted.xlsx) after each processed profile.
Implements error handling and resume capability (skips previously processed URLs).
5️⃣ Error Handling & Final Cleanup
Implements a retry mechanism in case of permission errors while saving Excel.
Ensures the browser (driver.quit()) is closed when done.
🔹 Why This Approach?
Headless Mode: Runs without opening the browser, making it faster.
Wait for Elements: Uses explicit waits to ensure elements are fully loaded before interaction.
Regex for Emails: Captures valid email formats efficiently.
Resume Functionality: Prevents duplicate processing if the script is interrupted.
Excel Storage: Saves extracted emails in an organized, readable format.
