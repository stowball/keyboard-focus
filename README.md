# Keyboard Focus

A rudimentary way to detect users that navigate with the Tab key to improve `:focus` styles for regular mouse and touch users.

## Installation instructions

* Download and include index.js; or
* install with [bower](https://bower.io) using `bower install keyboard-focus --save`

## What does it do?

A one-time event listener detects when a user presses Tab outside of form elements and adds a class of `.keyboard-focus` to `<html>` so you can target their focus styles specifically.

This allows you to prevent `:focus` styles from appearing on things like toggle buttons unless a user has pressed Tab, much like YouTube does with Play/Pause in its video player.

### Example usage

```css
/* Hide default :focus styles */
:focus {
    box-shadow: none;
    outline: none;
}

/* Apply a custom, generic :focus style for when JS isn't available or if a user has pressed Tab */
.no-js :focus,
.keyboard-focus :focus {
    box-shadow: 0 0 2px 1px #00cdcb;
}

/* Continue to add custom :focus styles for specific elements and components */
```
