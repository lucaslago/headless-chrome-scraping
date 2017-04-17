# headless-chrome-scraping

## Setup

1. Headless chrome is only available in Chrome Canary releases. Install it using brew:

```bash 
brew install Caskroom/versions/google-chrome-canary 
```

2. Find where the Chrome Canary binares are located:

```bash
sudo find / -type d -name "*Chrome Canary.app"
``` 

It will probably be located in `/Applications/Google/Chrome/Canary.app` for Mac users

3. Start chrome in headless mode: 

```bash
/Applications/Google\ Chrome\ Canary.app/Contents/MacOS/Google\ Chrome\ Canary --headless --remote-debugging-port=9222 --disable-gpu https://chromium.org
```

4. Execute the code in src folder using `node`. 
E.g: 
```bash
node ./src/image_tags.js
```
