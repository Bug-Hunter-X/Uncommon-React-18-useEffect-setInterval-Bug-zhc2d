# Uncommon React 18 useEffect setInterval Bug

This repository demonstrates a subtle bug that can occur when using `setInterval` within a `useEffect` hook in React 18 and higher.  React's automatic batching of state updates can lead to unexpected behavior if not handled correctly.

## Bug Description

The provided `bug.js` file shows an `setInterval` that continuously updates state without a cleanup function.  The effect is that the state updates pile up causing performance problems or unexpected behavior if the component unmounts before the interval is cleared.