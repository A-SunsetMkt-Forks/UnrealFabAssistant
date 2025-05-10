# UnrealFabAssistant

[简体中文](../README.md) | English

Automatically add all free resources from Fab to your account.(You can run it once in a while to automatically add the latest free resources)

>Note: The code has only been tested on Chrome, it is best to use Chrome directly.

### How to use

#### Method 1
1. Open Tampermonkey Settings-Utilities.
2. Paste the following link in **Install from URL** to import.
3. Open [Fab](https://www.fab.com/), click Start in the small window in the lower right corner, and wait for completion.
```javascript
https://raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/tampermonkey.js
```

#### Method 2
1. Open [Fab](https://www.fab.com/) and login.
2. Click F12 to open the debugger and switch to the Console tab.
3. Copy and paste the following code and press Enter to wait for the end.
```javascript
fetch('https://raw.githubusercontent.com/RyensX/UnrealFabAssistant/refs/heads/main/run.js').then(r=>r.text()).then(t=>document.head.append(Object.assign(document.createElement('script'),{textContent:t})))
```

#### Method 3
1. Open [run.js](/run.js) and copy all the code to the clipboard.
2. Open [Fab](https://www.fab.com/) and login.
4. Press F12 to open the debugger and switch to the Console tab.
5. Paste the code you just copied into the input box and press Enter.
6. Wait for the log to be printed  is complete.

### Known issues
- Too many requests prompt "Too many requests".
- If all storage has been completed, ignore it.
- If not, wait a few minutes and try again.

### Acknowledgements
- https://gist.github.com/jamiephan/0c04986c7f2e62d5c87c4e8c8ce115fc

### Others
1. If it helps you, please click ⭐ in the upper right corner to support it. Thank you for using it.
1. If you reprint it, please indicate the original source https://github.com/RyensX/UnrealFabAssistant
