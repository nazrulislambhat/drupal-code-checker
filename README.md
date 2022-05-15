# Drupal Code Quality Checker

---

## Overview

Provides set of libraries to easily setup code quality checks based on [GrumPHP](https://github.com/phpro/grumphp) for Drupal module/theme/profile. Check out this [Lullabot article](https://www.lullabot.com/articles/how-enforce-drupal-coding-standards-git) for more details.

> _Note:_ This library aim to help contributed/custom Drupal module/theme/profile hosted in individual git repository.

## Install

1. Add `nazrul/drupal-code-checker` to `composer.json` (like [here](https://github.com/nazrulislambhat/modal_config/blob/8.x-1.x/composer.json#L21)) or just `composer require --dev nazrul/drupal-code-checker`
2. Replace `grumphp.yml` in project's root directory (not Drupal root directory) with `vendor/nazrul/drupal-code-checker/grumphp.yml.dist`

That's it. Now, all tasks (listed below) run on every `git commit`.

> _Note:_ As part of install, GrumPHP adds `pre-commit` hook to repository. Existing `pre-commit` might get [destroyed](https://github.com/phpro/grumphp/issues/416) when install/uninstall.

## Features

1. [PHPCS](https://github.com/squizlabs/PHP_CodeSniffer) with Drupal standard.
1. [PHP Lint](http://www.icosaedro.it/phplint/)
1. [YAML Lint](http://www.yamllint.com/)
1. [Composer](https://github.com/composer/composer)
1. [Composer Normalize](https://github.com/ergebnis/composer-normalize)
1. [JSONLint](https://jsonlint.com/)
1. [PHP Copy/Paste Detector (CPD)](https://github.com/sebastianbergmann/phpcpd)

Long list of additional checks/validators available [here](https://github.com/phpro/grumphp/blob/master/doc/tasks.md#tasks-1).

## Sample

### Pass

![drupal-code-checker-pass](./docs/images/drupal-code-checker-pass.png)

### Fail

![drupal-code-checker-fail](./docs/images/drupal-code-checker-fail.png)

## Demo

Implemented in [Modal Configuration](https://github.com/nazrulislambhatislambhat/modal_config) module.

## Forked From

(https://github.com/vijaycs85/drupal-quality-checker)