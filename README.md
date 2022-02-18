<p align="center">
    <a href="https://sentry.io" target="_blank" align="center">
        <img src="https://sentry.io/_static/getsentry/images/branding/png/sentry-horizontal-black.png" width="280">
    </a>
</p>

# Sentry for 🛒 [OpenCart 2.3.x](https://github.com/opencart/opencart)

> "Sentry is a cross-platform 💥 crash reporting and aggregation platform".
For more information see official [Sentry repository](https://github.com/getsentry/sentry-php)

## Installation

1. Requiring installed [vQmod](https://github.com/vqmod/vqmod) because vQmod doesn't support installing via composer itself.
2. 💲 `composer require sasedev/composer-plugin-filecopier` for files manipulating
3. 💲 `composer require burdapraha/oc_sentry dev-master`
4. Add this code to your 🎵 composer.json project file, extra section:

```
    "extra": {
        "filescopier": [
            {
                "source": "vendor/burdapraha/oc_sentry/upload",
                "destination": "upload",
                "debug": "true"
            }
        ]
    }    
```
    
It will move vQmod xml file to correct folder.

5. add 🔑 constants to your `config.php` and `/admin/config.php`:

- `define('SENTRY_PHP', 'FILL_YOUR_ACCESS_PHP');`
- `define('SENTRY_JS', 'FILL_YOUR_ACCESS_JS');`

6. optionally you can add row to your `.gitignore` file with path to sentry.xml (example: upload/vqmod/xml/sentry.xml)
7. celebrate! 🎉 🎉 🎉

```
Запуск проекта:
cp .env.dist .env
cp traefic.toml.dist traefic.toml
touch acme.json
docker-compose -f prod.docker-compose.yml up -d
docker-compose -f proxy.yml up -d
```

