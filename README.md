# Current Site Version Compatibility and Provenance

This schema repo is currently updated to support version `1.141.1` of the site.

This schema is built from the original 5eTools Site Schema which can be found [here](https://github.com/5etools-mirror-1/5etools-mirror-1.github.io/tree/master/test/schema).

It further adapts the [main schema file](https://github.com/TheGiddyLimit/homebrew/blob/master/schema.json) from the homebrew repository that it aims to fully lint, which is available [here](https://github.com/TheGiddyLimit/homebrew).

## Important use instruction

If you want to use homebrew features of the schema, please do them last in each section you work with, that way you will get most out of the autocompletion for the non-homebrew specific features of the schema.

Example with `optionalfeature`:

```json
"optionalfeature": [
    {
        ...
            "featureType": [
                "PB",
                "IWM:W",
                "hello"   
            ],
        ...
    }
]

```

instead of:

```json
"optionalfeature": [
    {
        ...
            "featureType": [
                "PB",
                "hello",
                "IWM:W"  
            ],
        ...
    }
]
```

Here the schema provides a list of official feature types that you can choose from, which will disappear once you write down a homebrew feature type.

## 5eSchema for Editors

Just modified the actual 5e.tools Schema to one that can be used in your editor.

## How to use it with VS Code

- Download the folder with the schema
- Put it into a another folder in your VS Code Workspace
- Go to Settings and search for Schema
- Edit the settings.json for the JSON: Schemas setting
- Put this into your `"json.schemas"` array with your correct paths:

```json
{
    "fileMatch": [
        "*.json"
    ],
    "url": "./5etools-Homebrew-Schema/schema.json"
}
```

Every json file you make in this workplace folder now will use this schema.  
If something's missing or wrong let me know on Discord.
