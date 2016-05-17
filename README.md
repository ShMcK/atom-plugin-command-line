# Atom Plugin Command Line

Run a child process within an Atom plugin. Returns a promise with the output.

## Setup

`> npm install atom-plugin-command-line`

## Example

```javascript
import commandLine from 'atom-plugin-command-line';

function getNodeVersion() {
  return commandLine('node', '-v').then((res) => {
    if (!res) {
      console.log('Node not installed');
      return false;
    } else {
      return res.match(/([0-9]+)\.([0-9]+)/);
    }
  });
}
```
