[![npm version](https://badge.fury.io/js/event-target-fallback.svg)](https://badge.fury.io/js/event-target-fallback)
![Node.js CI](https://github.com/goldsrc/event-target-fallback/actions/workflows/test-on-node.yml/badge.svg)

# event-target-fallback

Forked from [event-target-polyfill](https://github.com/Raykeen/event-target-polyfill)

A fallback for `EventTarget` (and `Event`), meant to run in older version of node or possibly IE 11, that has the most accurate set of characteristics of `EventTarget` that can be provided.

If you find this implementation can be improved, please submit a PR and ping me [on Twitter via DM](https://twitter.com/mbeheshtis).

**NOTE**: If you are using Node 14 and higher, [EventTarget is available directly](https://nodejs.org/api/events.html#events_eventtarget_and_event_api) via experimental features\*\*
MDN: [EventTarget](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget)

## Usage

```
import 'event-target-fallback';

const et = new EventTarget();

et.addEventListener('test', () => console.log('hit!'));

et.dispatchEvent(new Event('test'));
```

## Development

This library has no dependencies. Even development dependencies. To test just run `npm test`. It runs a script, and if it finishes without error, the tests pass.

**NOTE**: run tests in node 14 or lower :)
