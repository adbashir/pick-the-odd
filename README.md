# pick-the-odd

**pick-the-odd** is a Python research tool for detecting algorithmic filtering or potential censorship in Facebook feeds.  
It logs in as multiple real users (with their consent), loads their home feeds, and checks whether a set of public posts appear for each user. This project helps surface disparities in what content is delivered to different users by the Facebook algorithm.

---

## Features

- Logs in with up to 10 real Facebook accounts (with user consent, via browser automation)
- Loads each user’s news feed in a secure, automated browser session
- Checks for the presence of user-specified public posts in each feed
- Outputs a matrix showing which posts appear (or do not appear) for which users
- Exports data for further analysis

---

## How it works

1. **Setup:** Collect explicit consent and credentials for 10 users (test or volunteer accounts only).
2. **Post Selection:** Identify 10 public Facebook posts (by URL or post ID) to track.
3. **Automation:** The tool logs in as each user (using Selenium or Playwright), loads their news feed, and scans for the selected posts.
4. **Reporting:** Results are saved as a table showing which users saw which posts in their feed.

---

## Example Output

| Post / User | User1 | User2 | User3 | ... | User10 |
|-------------|-------|-------|-------|-----|--------|
| Post A      |   ✓   |   ✓   |   ✗   | ... |   ✓    |
| Post B      |   ✓   |   ✗   |   ✓   | ... |   ✓    |
| ...         |  ...  |  ...  |  ...  | ... |  ...   |

---

## Installation

**Warning:**  
Use this tool only with explicit permission from all users.  
Intended for research and transparency work. May violate Facebook’s Terms of Service.

```bash
git clone https://github.com/yourusername/pick-the-odd.git
cd pick-the-odd
pip install -r requirements.txt
