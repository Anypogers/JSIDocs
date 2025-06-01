---
sidebar_position: 1
---

# Dynamic Configs

Dynamic Configs used by Just Simple Intens *or* other intents.

## Description

The dynamic configs used by JSI or intents.

You can add new configs to be used by your or other intents, or use existing intents.

## Default Configs

*Note: All Configs can also have it's value be null*

| Config Name | Value Type | Default Value |
|:------------|:-----------|:--------------|
| debugMode   | boolean    | false         |
| keyWord     | String     | null          |

## Methods

Getter:

```js
export function getDynamicConfig(configName) {
  
}
```

Setter:

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

Adder:

```js
export function addDynamicSetting(configname, configValue) {

}
```