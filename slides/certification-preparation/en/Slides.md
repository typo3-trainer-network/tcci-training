name: begin
class: center, middle, h1-fullwidth
background-image: url(../../images/TYPO3Logo.svg)

# TYPO3 Integrator Training

---
name: prerequirements
class: center, middle, h1-fullwidth
layout: false

# Prerequirements
---
name: webskills
class: h1-fullwidth
# Web skills

* HTML
* CSS
* Javascript
* SEO
---
name: technicalskills
class: h1-fullwidth
# Technical skills

* Charsets
* Command line
* File permissions
* Image manipulation
* Webserver
* Regular expressions
* YAML
* Cron jobs
* HTTP status codes
---
name: gettinghelp
class: center, middle, h1-fullwidth
layout: false

# Getting Help
---
name: documentation
class: h1-fullwidth
# Getting help

* docs.typo3.org
* Slack
* Mailing lists
* Stackoverflow [typo3]
---
name: installation
class: center, middle, h1-fullwidth
layout: false

# Installation
---
name: installrequirements
class: h1-fullwidth
# Software components

* Webserver
* PHP (Versions, Modules, Settings)
* DBMS
* Image manipulation libraries
* Commandline commands
* Operating systems
* Webbrowsers
---
name: installways
class: h1-fullwidth
# Installation ways

* get.typo3.org
    * composer
    * from Git
---
name: installtypo3
class: h1-fullwidth
# TYPO3 Tools

* Step wizard
* Upgrade wizard
* Install tool
* TYPO3 console
---
name: performance
class: center, middle, h1-fullwidth
layout: false

# Performance
---
name: performancex
class: h1-fullwidth
# performance

* Caching (Redis, Varnish)
* TYPO3 Caching
* HTTP headers
* compression / concatenating
---
name: backend-administration
class: center, middle, h1-fullwidth
layout: false

# Backend Administration
---
name: core
class: center, middle, h1-fullwidth
layout: false

# Core Architecture & APIs
---
name: typoscript
class: center, middle, h1-fullwidth
layout: false

# TypoScript
---
name: templating
class: center, middle, h1-fullwidth
layout: false

# Templating & other outputs
---
name: extensions
class: center, middle, h1-fullwidth
layout: false

# Extensions
---
name: security
class: center, middle, h1-fullwidth
layout: false

# Security
---
class: left, fullscreen-image pt-50
background-image: url(../../images/Benediktbeuern_1080p.png)

# Hallo schöne TYPO3 Welt!

## Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid animi aperiam aspernatur beatae blanditiis commodi deleniti dolores ducimus error ipsum iusto, obcaecati odio pariatur perspiciatis porro quasi quisquam reprehenderit suscipit.

---
class: right, fullscreen-image
background-image: url(../../images/Benediktbeuern_1080p.png)

# Hallo schöne TYPO3 Welt!

## Hier steht der Subheader ...

---
name: TOC
class: h1-fullwidth
# TOC

1. [Introduction](#intro)

--

2. [PSR Standards](#PSR)

--

3. Test

--

4. Text

--

5. Text

--

6. Text

--

7. Text

---
name: intro
class: h1-fullwidth

# Introduction

---
name: PSR
class: center, middle, h1-fullwidth
layout: false

# PSR standards

???

## Links

* [https://www.php-fig.org/psr/]()
* [https://en.wikipedia.org/wiki/PHP_Standard_Recommendation]()

---
name: PSR-1
class: h1-fullwidth

# PSR-1

???

# PSR-1 - Basic Coding Standard

It comprises what should be considered the standard coding elements that are required to ensure a high level of technical interoperability between shared PHP code.

## Links

* [https://www.php-fig.org/psr/psr-1/]()

--

## Basic Coding Standard

---
name: PSR-2
class: h1-fullwidth

# PSR-2

???

# PSR-2 - Coding Style Guide

It considers PSR-1 and it is intended to reduce cognitive friction when scanning code from different authors. It does so by enumerating a shared set of rules and expectations about how to format PHP code.

## Links

* [https://www.php-fig.org/psr/psr-2/]()

--

## Coding Style Guide

--

```php
class Foo
{
    public function bar()
	{
	    // …
	}
}
```

---
name: PSR-3
class: h1-fullwidth

# PSR-3

???

# PSR-3 - Logger Interface

It describes a common interface for logging libraries.

PSR-3 was implemented in TYPO3 Version 9.

## Links

* [https://www.php-fig.org/psr/psr-3/]()

--

## Logger Interface

---
name: PSR-4
class: h1-fullwidth

# PSR-4

???

# PSR-4 - Autoloading Standard

It describes a specification for autoloading classes from file paths. It is fully interoperable, and can be used in addition to any other autoloading specification, including PSR-0. This PSR also describes where to place files that will be auto loaded according to the specification.

## Links

* [https://www.php-fig.org/psr/psr-4/]()

--

## Autoloading Standard

--

(Replaced PSR-0)

---
name: PSR-7
class: h1-fullwidth

# PSR-7

## HTTP Message Interface

???

# PSR-7 - HTTP Message Interface

It describes common interfaces for representing HTTP messages as described in RFC 7230 and RFC 7231, and URIs for use with HTTP messages as described in RFC 3986.

## Links

* [https://www.php-fig.org/psr/psr-7/]()
* [https://docs.typo3.org/c/typo3/cms-core/master/en-us/Changelog/9.2/Feature-83736-ExtendedPSR-7RequestsWithTYPO3ServerParameters.html]()

--

The PSR-7 request objects created by TYPO3 now contain an instance of NormalizedParams which can be used instead of `GeneralUtility::getIndpEnv()` to access normalized server params.

```php
/** @var NormalizedParams $normalizedParams */
$normalizedParams = $request->getAttribute('normalizedParams');
$requestPort = $normalizedParams->getRequestPort();
```

---
name: PSR-11
class: h1-fullwidth

# PSR-11

???

# PSR-11 - Container Interface

It describes a common interface for dependency injection containers. The goal is to standardize how frameworks and libraries make use of a container to obtain objects and parameters (called entries in the rest of this document).

## Links

* [https://www.php-fig.org/psr/psr-11/]()
* [https://forge.typo3.org/issues/83968]()

--

## Container Interface

---
name: PSR-12
class: h1-fullwidth

# PSR-12

???

# PSR-12 - Extended Coding Style Guide

It extends, expands and replaces [PSR-2](#PSR-2), the coding style guide and requires adherence to [PSR-1](#PSR-1), the basic coding standard.

## Links

* [https://www.php-fig.org/psr/psr-12/]()

--

## Extended Coding Style Guide

--
```
<?php

declare(strict_types=1);

namespace Vendor\Package;

use Vendor\Package\{ClassA as A, ClassB, ClassC as C};
use Vendor\Package\SomeNamespace\ClassD as D;

use function Vendor\Package\{functionA, functionB, functionC};

use const Vendor\Package\{ConstantA, ConstantB, ConstantC};

class Foo extends Bar implements FooInterface
{
    public function sampleFunction(int $a, int $b = null): array
    {
        //…
```

---
name: PSR-14
class: h1-fullwidth

# PSR-14

???

# PSR-14 - Event Manager

It describes common interfaces for dispatching and handling events.

## Links:

* [https://www.php-fig.org/psr/psr-14/]()
* [https://docs.typo3.org/c/typo3/cms-core/master/en-us/Changelog/10.0/Feature-88770-PSR-14BasedEventDispatcher.html]()

--

## Event Manager

---
name: PSR-15
class: h1-fullwidth

# PSR-15

???
#PSR-15 - HTTP Server Request Handlers

It describes common interfaces for HTTP server request handlers and HTTP server middleware components that use HTTP messages.

## Links:

* [https://www.php-fig.org/psr/psr-15/]()

--

## HTTP Server Request Handlers

--

.center[![TYPO3 BE Configuration](../../images/TYPO3-BE-Configuration-PSR-15.png "TYPO3 BE Configuration Module")]

---
name: PSR-17
class: h1-fullwidth

# PSR-17

???

# PSR-17 - HTTP Factories 

It describes a common standard for factories that create PSR-7 compliant HTTP objects.

## Links

* [https://www.php-fig.org/psr/psr-17/]()
* [https://forge.typo3.org/issues/89018]()

--

## HTTP Factories

---
name: End
class: center, middle
count: false

.footnote[.red.bold[*]
Important footnote]

# End