Hamaco's PHP-CS-Fixer Rules
===========================

## Installation

```bash
$ composer repositories.hamaco/php-cs-fixer-rules vcs https://github.com/hamaco/php-cs-fixer-rules
$ composer require --dev hamaco/php-cs-fixer-rules:dev-master
```

## Setup

### Configuration

Create `.php-cs-fixer.dist.php`:

```php:.php-cs-fixer.dist.php
<?php

declare(strict_types=1);

return (new PhpCsFixer\Config())
    ->setRiskyAllowed(true)
    ->setRules((new Hamaco\PhpCsFixer\Rules())->getRules())
    ->setFinder(PhpCsFixer\Finder::create()->exclude('vendor')->in(__DIR__));
```


### Git

Add PHP-CS-Fixer cache file to `.gitignore`:

```.gitignore
+ /.php-cs-fixer.cache
```
