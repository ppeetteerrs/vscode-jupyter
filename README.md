# Fixes
1. Changed Notebook code executions from `Promise.all` to a sequence of `await`s with a 50ms delay
    - Resolved issue of race condition output `msg_id` (likely due to VSCode doing some more async stuff before sending message to kernel, which is causes synchronization issues)

# Prebuilt VSIX
- In release page
- In `release` folder

# Local Build
- `npm install -g vsce`
- Change "engines" in `package.json` to desired VSCode version
- `npm ci && npm run clean && npm run package`
