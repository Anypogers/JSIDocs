---
sidebar_position: 2
---

# Static Configs

Static Configs used by Just Simple Intens *or* other intents.

## Description

The static configs used by JSI or intents.

You can add new configs to be used by your or other intents, or use existing intents.

## Default Configs

*Note: All Configs can also have it's value be null*

| Config Name   | Value Type     | Default Value |
|:--------------|:---------------|:--------------|
| threshold     | Number         | 0.90          |
| languages     | Array (String) | ['en']        |
| forceNER      | Boolean        | true          |
| intentsPath   | String         | './intents/'  |
| defaultIntent | String         | null          |


## Methods

There are 3 methods for the the static configs, the **getter**, **setter**, and **adder**

### Getter

```js
getStaticConfig("threshold");
```

#### Method:

```js
export function getStaticConfig() {
  
}
```

### Setter

```js
setStaticConfig("threshold", 0.95);
```

#### Method:

```js
export function setStaticConfig(configName, configValue) {
  // Check if the config name is valid
  if (!staticConfig.hasOwnProperty(configName)) {
    throw new Error(`Invalid config name: ${configName}`);
  }

  // Check if the config value is valid
  if ((typeof configValue) !== (typeof staticConfig[configName]) && configValue !== null) {
    throw new Error(`Invalid config value: ${configValue} for config name: ${configName}`);
  }
  
  staticConfig[configName] = configValue;
}
```

### Adder

```js
addStaticConfig('myStaticValue', 'Hello, World!');
```

#### Method:

```js
export function addStaticConfig() {
  
}
```