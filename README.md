# three-devtools

**three-devtools** is a web extension that allows inspection of three.js content.

> ## 🚨 Status: Experimental
> **three-devtools** is very much in an alpha/experimentation stage. Use at your own risk. Follow the [Baseline Milestone](https://github.com/jsantell/three-devtools/milestone/1) for issues and considerations that need to be solved in order for some stability.

## Current API

This API has not been thought out at all, but this will register your
THREE.Scene and THREE.Renderer to be observed by the tools.

```js
// Track a scene or a renderer
if (typeof __THREE_DEVTOOLS__ !== 'undefined') {
  __THREE_DEVTOOLS__.dispatchEvent(new CustomEvent('track', { detail: scene }));
  __THREE_DEVTOOLS__.dispatchEvent(new CustomEvent('track', { detail: renderer }));
}
```

## Development

Architecture & development notes can be found in [DEVELOPMENT.md](DEVELOPMENT.md).
