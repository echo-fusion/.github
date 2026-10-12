# EchoFusion

**A modular PHP framework, built from small packages that work well alone and even better together.**

Every EchoFusion module is a standalone Composer package built on PSR standards (PSR-7, PSR-11, PSR-15). Use one piece in your own project, or combine them into a full framework.

## Design in one minute

* **Modules depend on `contracts`, not on each other.** Shared interfaces live only in [`contracts`](https://github.com/echo-fusion/contracts), so any module can be replaced by another implementation (your own, or a third-party library such as Doctrine) without touching the code that uses it.
* **Small and readable.** Each package does one job and is small enough to read in an afternoon.
* **Tested on every supported PHP version.** PHP 8.1, 8.2 and 8.3, against the locked, the lowest and the highest allowed `contracts` version.

## Packages

### Foundation

| Package | What it does |
| --- | --- |
| [`contracts`](https://github.com/echo-fusion/contracts) | Shared interfaces for every module (the glue of the framework) |
| [`codestandard`](https://github.com/echo-fusion/codestandard) | Shared code style rules (PHP CS Fixer) |

### HTTP and application core

| Package | What it does |
| --- | --- |
| [`routemanager`](https://github.com/echo-fusion/routemanager) | HTTP router with PSR-7/PSR-15 and middleware support |
| [`middlewaremanager`](https://github.com/echo-fusion/middlewaremanager) | PSR-15 middleware manager and pipeline |
| [`servicemanager`](https://github.com/echo-fusion/servicemanager) | PSR-11 service container with lazy loading and service providers |
| [`eventmanager`](https://github.com/echo-fusion/eventmanager) | Event dispatching with listeners and priorities |
| [`pluginmanager`](https://github.com/echo-fusion/pluginmanager) | Plugin loading and registration per environment |
| [`modulemanager`](https://github.com/echo-fusion/modulemanager) | Module registry: config, providers, routes and templates declared as data |

### Services

| Package | What it does |
| --- | --- |
| [`configmanager`](https://github.com/echo-fusion/configmanager) | Immutable configuration with deep merge and dot-notation access |
| [`sessionmanager`](https://github.com/echo-fusion/sessionmanager) | Native and in-memory sessions, flash messages, PSR-15 start-session middleware |
| [`responsemanager`](https://github.com/echo-fusion/responsemanager) | PSR-7 HTML, JSON, XML and redirect responses |
| [`templatemanager`](https://github.com/echo-fusion/templatemanager) | Own template language, plain PHP templates, optional Twig or any engine through configuration |
| [`databasemanager`](https://github.com/echo-fusion/databasemanager) | PDO connection, query builder and named connections behind one contract; Doctrine DBAL adapter included |
| [`authmanager`](https://github.com/echo-fusion/authmanager) | Session and token authentication with pluggable guards and user providers |

### The framework and the project template

| Package | What it does |
| --- | --- |
| [`framework`](https://github.com/echo-fusion/framework) | The kernel: boots configuration, modules, providers, events and plugins, and turns a PSR-7 request into a response |
| [`echo-fusion`](https://github.com/echo-fusion/echo-fusion) | The project skeleton you start an application from |

## Start a project

```bash
composer create-project echo-fusion/echo-fusion my-app
cd my-app
composer serve          # http://localhost:8000
```

Prefer to start from a finished application (accounts, posts, an admin panel, a JSON API, demo data)?

```bash
composer create-project echo-fusion/echo-fusion my-blog dev-blog
```

## Learn

* [Documentation](https://github.com/echo-fusion/framework/tree/main/docs): routing, controllers and the `Request`, templates, database and migrations, authentication, CSRF, the command line, testing, deployment
* [Tutorial: how the example blog works](https://github.com/echo-fusion/framework/blob/main/docs/tutorial-blog.md)

## Use only what you need

Every package works on its own:

```bash
composer require echo-fusion/routemanager
composer require echo-fusion/servicemanager
```

All packages are published on [Packagist](https://packagist.org/packages/echo-fusion/).

## Requirements

PHP 8.1, 8.2 or 8.3.

## Maintainer

Created and maintained by [Amir Shadanfar](https://github.com/amir-shadanfar). Issues and pull requests are welcome in the individual repositories.

The first, monolithic version of the project is kept, archived, in [echo-php](https://github.com/echo-fusion/echo-php).
