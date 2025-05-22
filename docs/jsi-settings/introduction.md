---
sidebar_position: 1
---

# Introduction

### Getting

To get the functions,

```js
import {getConfig} from '<path-to-src/config.js>'

// Note that static config is the default type for a config to be

getConfig('intentsPath') // returns the intents path (static config)
getConfig('keyWord', 'dynamic') // returns the word used for wake calls (dynamic config)
getConfig('forceNER', 'static') // returns if it should force use Named Entity Recognition (static config)
```

___

### Getter

**Getter function used for both functions**

```js
export function getConfig(configName, type = 'static') {
  // Check if the config type is valid
  if (type !== 'static' && type !== 'dynamic') {
    throw new Error(`Invalid config type: ${type}`);
  }

  const configSet = type === 'static' ? staticConfig : dynamicConfig;
  
  // Check if the config name is valid
  if (!configSet.hasOwnProperty(configName)) {
    throw new Error(`Invalid config name: ${configName} (Not found in ${type} config)`);
  }

  let value = configSet[configName];

  // Automatically resolve intentsPath to absolute when requested
  if (type === 'static' && configName === 'intentsPath') {
    value = path.isAbsolute(value)
      ? value
      : path.resolve(process.cwd(), value); // resolves relative to where the program is run
  }

  return value;
}
```