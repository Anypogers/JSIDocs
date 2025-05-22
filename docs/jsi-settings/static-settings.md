```js
const staticConfig = {
  // Minimum confidence threshold for intent recognition
  // default = 0.90
  threshold: 0.90,

  // The languages to be used for the NLP manager
  // default = ['en']
  languages: ['en'],

  // Force NER (Named Entity Recognition) to be used even if there are no entities in the input
  // default = true
  forceNER: true,

  // The path to the intents folder
  // default = './intents/'
  intentsPath: './intents/',

  // Default intent if no other intent is recognized
  // (make it null to do nothing if no intent is recognized)
  // default = null
  defaultIntent: null,
}
```

### Setter

**Setter function used for the static configs**

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