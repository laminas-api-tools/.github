# Renovate

This repository extends the Laminas shared configuration providing a Laminas API Tools configuration for Renovate. See
the [Laminas](https://github.com/laminas/.github/RENOVATE.md) documentation for further information.

## Next steps for downstream maintainers

Once the WhiteSource Renovate GitHub app is enabled for a repository, a new `Configure Renovate` PR will be opened
containing a basic `renovate.json` file with the following contents:

```json
{
    "extends": [
        "local>laminas-api-tools/.github:renovate-config"
    ]
}
```

In order to be fully compatible with this Renovate configuration, you must ensure the following criteria are met:
1. CI actions are enabled for `push` events on branches with the prefix `renovate/*`.
2. The lockfile must have been generated using Composer with a version `>=2.2`.
3. Lastly, for Renovate to detect the correct version of PHP to use for lockfile maintenance, the PHP version must be
   set in `composer.json` under the key [`config.platform.php`](https://getcomposer.org/doc/06-config.md#platform).

## Links

[Renovate on GitHub](https://github.com/renovatebot/renovate)
[Renovate Documentation](https://docs.renovatebot.com)
[WhiteSource Renovate website](https://www.whitesourcesoftware.com/free-developer-tools/renovate/)
[WhiteSource Renovate GitHub app](https://github.com/marketplace/renovate)
