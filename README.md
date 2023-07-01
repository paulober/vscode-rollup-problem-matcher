# Rollup Problem Matcher

A problem matcher for the Rollup CLI. Currently only supports Typescript and the -watch option.

## Requirements

For rollup typescript watch to work you need to use the `@rollup/plugin-typescript` plugin.

## Usage

You can use this problem matcher in your `rollup -w` tasks like so:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "type": "npm",
      "script": "watch",
      "isBackground": true,
      "problemMatcher": "$rollup-ts-watch",
      "presentation": {
        "reveal": "never"
      },
      "group": {
        "kind": "build",
        "isDefault": true
      }
    }
  ]
}
```

or

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "rollup",
      "type": "shell",
      "command": "rollup -c -w",
      "problemMatcher": ["$rollup-ts-watch"]
    }
  ]
}
```
