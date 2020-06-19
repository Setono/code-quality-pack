# Code Quality Pack
A Symfony pack that requires code quality tools.

```bash
$ composer require --dev setono/code-quality-pack
```

## Packages

* [ergebnis/composer-normalize](https://github.com/ergebnis/composer-normalize)
    * Normalizes your `composer.json`. This has a few advantages - easier diffs  being one of them.
* [phpstan/phpstan](https://github.com/phpstan/phpstan)
    * A static analysis tool.
* [korbeil/phpstan-generic-rules](https://github.com/Korbeil/phpstan-generic-rules)
    * Has some very simple phpstan rules, i.e. it finds usages of debug functions like `dd` and reports them.
* [phpstan/phpstan-doctrine](https://github.com/phpstan/phpstan-doctrine)
    * Doctrine extensions for PHPStan.
* [phpstan/phpstan-strict-rules](https://github.com/phpstan/phpstan-strict-rules)
    * Strict PHPStan rules.
* [phpstan/phpstan-webmozart-assert](https://github.com/phpstan/phpstan-webmozart-assert)
    * [webmozart/assert](https://github.com/webmozart/assert) extension for PHPStan.
* [phpstan/extension-installer](https://github.com/phpstan/extension-installer)
    * Automatically installs PHPStan extensions. This makes sure that all extensions are installed automatically and you
    don't have to add them to your `phpstan.neon` config.
* [sylius-labs/coding-standard](https://github.com/SyliusLabs/CodingStandard)
    * Sylius' coding standard. Very thorough.
* [thecodingmachine/phpstan-safe-rule](https://github.com/thecodingmachine/phpstan-safe-rule)
    * A PHPStan rule that reports usage of functions which that can return arbitrary results instead of throwing exceptions.