# HocCungAI Listeners Remover Instructions
this guide provides to you way to remove some "UNWANTED" event listeners from that website. make you can out the tab without any warns
## This script Works on:
- **HocCungAI**:`https://hoccungai.vn/*`
## Steps:
1.**(If it requires)Allow pasting it first**
    ```javascript
    allow pasting
    ```
2. **Copy the Script Before Going Into the test**
    ```javascript
const targets = [
  ["document", document, "visibilitychange"],
  ["document", document, "fullscreenchange"],
  ["document", document, "fullscreenerror"],
  ["document", document, "paste"],
  ["document", document, "copy"],
  ["document", document, "cut"],
  ["window", window, "blur"],
  ["window", window, "focus"]
];

for (const [scope, obj, event] of targets) {
try {
  (getEventListeners(obj)[event] || []).forEach(x => {
    obj.removeEventListener(event, x.listener, x.useCapture);
    console.log("H.B.G has removed", x.listener);
  });
} catch (e) {
  console.log("You are cooked buddy")
  }
}
    ```
3. Go To The Test When it show like this
<img width="1426" height="795" alt="image" src="https://github.com/user-attachments/assets/637829f3-e5f8-4c42-b880-aa0d44d77a1a" />
then press

| Operating System | Keys |
| :----------------: | :----: |
| macOS | <kbd>alt</kbd><kbd>cmd</kbd><kbd>i</kbd> |
| Windows | <kbd>ctrl</kbd><kbd>shift</kbd><kbd>i</kbd> |
| Linux | <kbd>ctrl</kbd><kbd>shift</kbd><kbd>i</kbd> |

and paste the code and press **enter** it should show something like this:
<img width="1041" height="802" alt="image" src="https://github.com/user-attachments/assets/8a18d5b7-aa96-4671-8923-9bc15eb8fc6d" />
## Disclaimer:
- The author is not responsible for misusing this script.
