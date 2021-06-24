The logging setup I use with galaxy_ng
https://github.com/ansible/galaxy_ng

logging.yaml is the main config.
There are few other stripped down logging_*.yaml
configs as well.

# To use the logging.yaml here for galaxy_ng

1. Install the deps
2. cp logging.yaml and settings_logging.py to
   galaxy_ng/app/
3. Update galaxy_ng/app/settings.py to include this
   code at/near the top

```
from galaxy_ng.app import settings_logging

LOGGING = settings_logging.LOGGING
```

# deps

See requirements.txt

But includes:

- https://github.com/alikins/color_bucket_logger
- https://github/com/alikins/alogging

