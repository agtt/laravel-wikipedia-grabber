# Laravel Wikipedia Grabber

[![StyleCI](https://styleci.io/repos/117998599/shield?branch=master&style=flat)](https://styleci.io/repos/117998599)
[![Build Status](https://travis-ci.org/dmitry-ivanov/laravel-wikipedia-grabber.svg?branch=master)](https://travis-ci.org/dmitry-ivanov/laravel-wikipedia-grabber)
[![Coverage Status](https://coveralls.io/repos/github/dmitry-ivanov/laravel-wikipedia-grabber/badge.svg?branch=master)](https://coveralls.io/github/dmitry-ivanov/laravel-wikipedia-grabber?branch=master)

[![Latest Stable Version](https://poser.pugx.org/illuminated/wikipedia-grabber/v/stable)](https://packagist.org/packages/illuminated/wikipedia-grabber)
[![Latest Unstable Version](https://poser.pugx.org/illuminated/wikipedia-grabber/v/unstable)](https://packagist.org/packages/illuminated/wikipedia-grabber)
[![Total Downloads](https://poser.pugx.org/illuminated/wikipedia-grabber/downloads)](https://packagist.org/packages/illuminated/wikipedia-grabber)
[![License](https://poser.pugx.org/illuminated/wikipedia-grabber/license)](https://packagist.org/packages/illuminated/wikipedia-grabber)

Provides convenient way to grab Wikipedia (or another MediaWiki) page.

| Laravel | Wikipedia Grabber                                                            |
| ------- | :--------------------------------------------------------------------------: |
| 5.5.*   | [5.5.*](https://github.com/dmitry-ivanov/laravel-wikipedia-grabber/tree/5.5) |

## Table of contents

- [Usage](#usage)
- [Languages](#languages)
- [Formats](#formats)
- [Methods](#methods)
- [Advanced](#advanced)
  - [MediaWiki](#mediawiki)
  - [Configuration](#configuration)
  - [Add custom sections](#add-custom-sections)

## Usage

1. Install package through `composer`:

    ```shell
    composer require illuminated/wikipedia-grabber
    ```

2. Use `Wikipedia` class:

    ```php
    echo (new Wikipedia)->page('Donald Trump');
    ```

    Live demo would be added here soon.

## Languages

> Only `en` and `ru` languages are supported now.

Default language is English. However, you can change it:

```php
echo (new Wikipedia('ru'))->page('Donald Trump');
```

## Formats

These formats are supported now:

- `plain` (default)
- `bulma` (see [Bulma](https://bulma.io))
- `bootstrap` (see [Bootstrap 3](https://getbootstrap.com/docs/3.3/), [Bootstrap 4](https://getbootstrap.com))

You can change format in your config (see [Configuration](#configuration)):

```php
return [

    'format' => 'bulma',

];
```

Or on the fly:

```php
echo (new Wikipedia)->page('Donald Trump')->plain();
echo (new Wikipedia)->page('Donald Trump')->bulma();
echo (new Wikipedia)->page('Donald Trump')->bootstrap();
```
