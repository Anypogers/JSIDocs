```js
const dynamicConfig = {
  // Logs important information to the console
  // (such as accuracy, the intent recognized, etc.)
  // (useful for debugging and testing)
  // default = false
  debugMode: false,

  // The keyWord to be used for the wake word detection
  // (if the wake word detection is enabled)
  // (make it null to disable the wake word detection, and only activate when called via code)
  // default = null
  keyWord: null,
}
```

## Setter

**Setter function used for the dynamic configs**

```js
export function setDynamicConfig(configName, configValue) {
  // Check if the config name is valid
  if (!dynamicConfig.hasOwnProperty(configName)) {
    throw new Error(`Invalid config name: ${configName}`);
  }

  // Check if the config value is valid
  if ((typeof configValue) !== (typeof dynamicConfig[configName]) && configValue !== null) {
    throw new Error(`Invalid config value: ${configValue} for config name: ${configName}`);
  }

  dynamicConfig[configName] = configValue;
}
```