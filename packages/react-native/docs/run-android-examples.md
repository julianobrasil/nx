`project.json`:

```json
{
  "name": "mobile",
  //...
  "targets": {
    //...
    "run-android": {
      "executor": "@nrwl/react-native:run-android",
      "options": {}
    }
  }
}
```

```bash
nx run mobile:run-android
```

## Examples

{% tabs %}
{% tab label="Run on a specific device/simulator" %}
To see all the avaiable emulators, run command:

```bash
emulator -list-avds
```

The `deviceId` option allows you to launch your android app in a specific device/simulator:

```json
    "run-android": {
      "executor": "@nrwl/react-native:run-android",
      "options": {
        "deviceId": "Pixel_5_API_30"
      }
    }
```

{% /tab %}
{% tab label="Run the debug/release app" %}
The `variant` option allows to specify the build variant, such as `debug` or `release`.

```json
    "run-android": {
      "executor": "@nrwl/react-native:run-android",
      "options": {
        "variant": "release"
      }
    }
```

{% /tab %}
{% /tabs %}

---
