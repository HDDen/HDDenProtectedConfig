# HDDen Protected Config

Simple PHP class for storing config files inside protected PHP containers.

## Install

In composer.json:

```json
"repositories": [
    {
        "type": "git",
        "url": "https://github.com/HDDen/HDDenProtectedConfig.git"
    }
],
...
"require": {
    "hdden/hdden-protected-config": "^2.0"
}
```

Install to project:

```bash
composer require hdden/hdden-protected-config
```

## Usage

```php
use HDDen\ProtectedConfig\HDDenProtectedConfig;

$config_entity = new HDDenProtectedConfig(__DIR__.'/config.json.php');

$data = $config_entity->read($onlycontent=true);
$data = ['foo' => 'bar'];
$config_entity->store($data);
```
