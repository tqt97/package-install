## Package useful in application laravel version 10+

<details>

<summary><b>Laravel Pint</b></summary>

### Install  [🔗](https://laravel.com/docs/10.x/pint)
```
    composer require laravel/pint --dev
```

### Add to composer.json
```md
    "scripts": {
        ...
        "post-create-project-cmd": [
            "@php artisan key:generate --ansi"
        ],
        "format": ["./vendor/bin/pint"],
    }
```

</details>

<details>

<summary> <b>Larasan</b> </summary>

### Install  [🔗](https://github.com/nunomaduro/larastan)
```
    composer require nunomaduro/larastan:^2.0 --dev
```
Then, create a phpstan.neon or phpstan.neon.dist file in the root of your application. It might look like this:
```
    includes:
        - ./vendor/nunomaduro/larastan/extension.neon

    parameters:

        paths:
            - app/

        # Level 9 is the highest level
        level: 5

    #    ignoreErrors:
    #        - '#PHPDoc tag @var#'
    #
    #    excludePaths:
    #        - ./*/*/FileToBeExcluded.php
    #
    #    checkMissingIterableValueType: false
```

### Add to composer.json
```md
    "scripts": {
        ...
        "post-create-project-cmd": [
            "@php artisan key:generate --ansi"
        ],
        "analyze": ["./vendor/bin/phpstan analyse"],
    }
```

</details>