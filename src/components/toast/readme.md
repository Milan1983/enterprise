---
title: Toast Component
description: This page describes Toast Component .
demo:
  pages:
  - name: Common Configuration
    slug: example-index
  - name: Demo of all Positions
    slug: example-positions
---

## Behavior Guidelines

This component is used to read out the error messages for validation as well.

## Code Example

The toast component is a JS-based component that lets you send a quick feedback message to the user. The message will display and timeout after 6s, showing a progress bar with an option to immediately dismiss. To show a test message, call the toast function on the body element passing in the title and message content.

```javascript
//Show a Visual Toast Message
$('body').toast({
  title: 'Application Offline',
  message: 'This is a Toast message'
});
```

## Accessibility

The toast component is made accessible by making an aria live region which means the attribute `aria-live="polite"` is added. Because of this, the control can actually be used to announce/read out something to a screen reader. You can do this by passing the `audible: true` setting. Because the message is polite, it will be read after the user is done with the current actions.

## Responsive Guidelines

- Will be placed in the top corner by default.

## Testability

- Please refer to the [Application Testability Checklist](https://design.infor.com/resources/application-testability-checklist) for further details.

## Upgrading from 3.X

- Replaced `inforSlideInMessage()` so rename that to `toast()`.
- Change option `messageTitle` to `title`.
- `MessageType` is not used.
- `scr-errors` is not required to be added to the DOM.
