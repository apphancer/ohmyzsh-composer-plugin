# Composer aliases and command completion for Oh My Zsh

This plugin provides completion for [composer](https://getcomposer.org/), as well as aliases
for frequent composer commands. It also adds Composer's global binaries to the PATH, using
Composer if available.


This is a modified version of the original https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/composer
It runs all composer commands from [symfony/cli](https://github.com/symfony/cli), i.e. without memory limit and with PHP version specified for current project


## Installation

To use it add `symfony-composer` to the plugins array in your zshrc file.

```zsh
plugins=(... symfony-composer)
```


## Aliases

| Alias  | Command                                      | Description                                                                             |
| ------ | -------------------------------------------- | --------------------------------------------------------------------------------------- |
| `c`    | `symfony composer`                           | Starts composer                                                                         |
| `csu`  | `symfony composerself-update`                | Updates composer to the latest version                                                  |
| `cu`   | `symfony composerupdate`                     | Updates composer dependencies and `composer.lock` file                                  |
| `cr`   | `symfony composerrequire`                    | Adds new packages to `composer.json`                                                    |
| `crm`  | `symfony composerremove`                     | Removes packages from `composer.json`                                                   |
| `ci`   | `symfony composerinstall`                    | Resolves and installs dependencies from `composer.json`                                 |
| `ccp`  | `symfony composercreate-project`             | Create new project from an existing package                                             |
| `cdu`  | `symfony composerdump-autoload`              | Updates the autoloader                                                                  |
| `cdo`  | `symfony composerdump-autoload -o`           | Converts PSR-0/4 autoloading to classmap for a faster autoloader (good for production)  |
| `cgu`  | `symfony composerglobal update`              | Allows update command to run on COMPOSER_HOME directory                                 |
| `cgr`  | `symfony composerglobal require`             | Allows require command to run on COMPOSER_HOME directory                                |
| `cgrm` | `symfony composerglobal remove`              | Allows remove command to run on COMPOSER_HOME directory                                 |
| `cget` | `curl -s https://getcomposer.org/installer`  | Installs composer in the current directory                                              |
| `co`   | `symfony composeroutdated`                   | Shows a list of installed packages with available updates                               |
| `cod`  | `symfony composeroutdated --direct`          | Shows a list of installed packages with available updates which are direct dependencies |
