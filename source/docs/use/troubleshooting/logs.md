---
title: Log file and debug logging
description: "Enabling debug logging"
---

Like any other integration, the HACS integration logs to the `home-assistant.log` file.

To enable `debug` logging, add this to your [`configuration.yaml`](https://www.home-assistant.io/docs/configuration/):

```yaml title="configuration.yaml"
logger:
  default: info
  logs:
    custom_components.hacs: debug
    aiogithubapi: debug
```

The logs created via [**Enable debug logging**](https://www.home-assistant.io/docs/configuration/troubleshooting/#debug-logs-and-diagnostics) button only include the `custom_components.hacs` logs, but not other parts like `aiogithubapi` or logs written during start up. For this reason, you need to define debug logging in your [`configuration.yaml`](https://www.home-assistant.io/docs/configuration/) file. Don't forget to remove the entry once your done troubleshooting.