# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Composer meta-package (`setono/code-quality-pack`) that bundles PHP code quality tools into a single dev dependency. It contains no source code — only `composer.json` defining the bundled tools:

- **ergebnis/composer-normalize** — composer.json normalization
- **infection/infection** — mutation testing
- **phpstan/phpstan** — static analysis
- **phpstan/phpstan-strict-rules** — strict PHPStan rules
- **rector/rector** — automated refactoring
- **sylius-labs/coding-standard** — coding standards (PHP CodeSniffer based)

## Commands

```bash
# Install dependencies
composer install

# Validate composer.json
composer validate --strict

# Check composer.json normalization
composer normalize --dry-run

# Apply composer.json normalization
composer normalize
```

## CI

The GitHub Actions workflow (`.github/workflows/build.yaml`) runs on PHP 8.2–8.4 and validates `composer.json` (strict mode + normalization check). There are no tests to run.

## Important Workflow

When adding, removing, or changing dependencies in `composer.json`, always update `README.md` to reflect the current package list.

## Notes

- The `dealerdirect/phpcodesniffer-composer-installer` plugin is explicitly disallowed in composer config
