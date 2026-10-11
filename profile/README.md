# EchoFusion

**A modular PHP framework, built from small packages that work well alone and even better together.**

Every EchoFusion module is a standalone Composer package built on PSR standards (PSR-7, PSR-11, PSR-15). Use one piece in your own project, or combine them into a full framework. All modules share a single set of interfaces, so they stay interchangeable.

## Packages

| Package | What it does |
| --- | --- |
| [`contracts`](https://github.com/echo-fusion/contracts) | Shared interfaces for every module (the glue of the framework) |
| [`routemanager`](https://github.com/echo-fusion/routemanager) | Lightweight HTTP router with PSR-7/PSR-15 and middleware support |
| [`middlewaremanager`](https://github.com/echo-fusion/middlewaremanager) | PSR-15 middleware manager and pipeline |
| [`servicemanager`](https://github.com/echo-fusion/servicemanager) | PSR-11 service container with lazy loading and service providers |
| [`eventmanager`](https://github.com/echo-fusion/eventmanager) | Event dispatching with listeners and priorities |
| [`pluginmanager`](https://github.com/echo-fusion/pluginmanager) | Plugin loading and registration per environment |
| [`codestandard`](https://github.com/echo-fusion/codestandard) | Shared code style rules (PHP CS Fixer) |

More modules (configuration, sessions, responses, modules) are on the way, together with the `framework` package and the `echo-fusion` project skeleton.

## Install

```bash
composer require echo-fusion/routemanager
composer require echo-fusion/servicemanager
```

All packages are published on [Packagist](https://packagist.org/packages/echo-fusion/).

## Requirements

PHP 8.1, 8.2 or 8.3.

## Maintainer

Created and maintained by [Amir Shadanfar](https://github.com/amir-shadanfar). Issues and pull requests are welcome in the individual repositories.
