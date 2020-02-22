name: begin
class: center, middle, h1-fullwidth
background-image: url(../../images/TYPO3Logo.svg)

# TYPO3 Integrator Training

---
name: agenda
class: h1-fullwidth
# Agenda

* [Introduction](#introduction)
* [Prerequirements](#prerequirements)
* [Getting Help](#gettinghelp)
* [Installation](#installation)
* [Performance](#performance)
* [Backend Administration](#backend-administration)
* [Core Architecture & APIs](#core)
* [TypoScript](#typoscript)
* [Templating & other outputs](#templating)
* [Extensions](#extensions)
* [Security](#security)
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
???
* you know HTML5 tags and understand semantic HTML
* you know what HTML-attributes are

--

* CSS
???
* you know how to include CSS in different ways
--

* Javascript
???
* you know how to include JS in different ways
* you know that there exist different javascript libraries

--

* SEO
???
* you know about meta tags
* you know what a XML sitemap is
* you know about speaking urls and redirects
* you know about important texts (page title, title attribute, ...)
* you know index-enable, follow, robots.txt, canonical, hreflang

---
name: technicalskills
class: h1-fullwidth
# Technical skills

* Charsets

--

* Command line

--

* File permissions

--

* Image manipulation

--

* Webserver

--

* Regular expressions

--

* YAML

--

* Cron jobs

--

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

--

* Slack

--

* Mailing lists

--

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

--

* PHP (Versions, Modules, Settings)

--

* DBMS

--

* Image manipulation libraries

--

* Commandline commands

--

* Operating systems

--

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

--

* Upgrade wizard

--

* Install tool

--

* TYPO3 console
---
name: performance
class: center, middle, h1-fullwidth
layout: false

# Performance
---
name: performancex
class: h1-fullwidth
# Performance

* Caching (Redis, Varnish)

--

* TYPO3 Caching

--

* HTTP headers

--

* compression / concatenating
---
name: backend-administration
class: center, middle, h1-fullwidth
layout: false

# Backend Administration
---
name: backend-administrationx
class: h1-fullwidth
# Backend Administration

* Site Configuration

--

* Workspaces

--

* Forms

--

* Import/Export

--

* User Rights/Access

--

* Rich text editor

--

* Reports Module

--

* Scheduler
---
name: core
class: center, middle, h1-fullwidth
layout: false

# Core Architecture & APIs
---
name: corex
class: h1-fullwidth
# Core Architecture & APIs

* FAL

--

* XLIFF

--

* Page title provider
---
name: typoscript
class: center, middle, h1-fullwidth
layout: false

# TypoScript
---
name: typoscriptx
class: h1-fullwidth
# TypoScript

* TypoScript functions (getText, stdWrap, ...)

--

* Image Generation / Manipulation with TypoScript

--

* TypoScript Constants

--

* TypoScript Object Browser / Template Analyzer

--

* TypoScript Syntax & Basics & TLOs

--

* Page & User TSconfig

--

* TypoScript Objects and properties
---
name: templating
class: center, middle, h1-fullwidth
layout: false

# Templating & other outputs
---
name: templatingx
class: h1-fullwidth
# Templating & other outputs

* What is a Templating Engine?

--

* What is Fluid?

--

* ViewHelpers

--

* Importing ViewHelpers

--

* Templates, Layouts, Partials

--

* Using the Fluid View

--

* Fluid ViewHelpers

--

* Dataprocessors
---
name: extensions
class: center, middle, h1-fullwidth
layout: false

# Extensions
---
name: extensionsx
class: h1-fullwidth
# Extensions

* Extension Manager Basics

--

* Composer

--

* TER

--

* Plugins and Modules

--

* What is MVC?
---
name: security
class: center, middle, h1-fullwidth
layout: false

# Security
---
name: securityx
class: h1-fullwidth
# Security

* About the TYPO3 Security Team

???

* How to deal with security issues, both found and reported.

* How to contact security team

--

* Get informed about Security issues

???

* RSS Feed (https://typo3.org/help/security-advisories/)

* Mailing List (http://lists.typo3.org/cgi-bin/mailman/listinfo/typo3-announce)

* Extension Manager + Scheduler Tasks
  (Update extension manager list + send email on system report issues)

--

* Secure passwords

--

* Security inside TypoScript and Fluid

???

* Know https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html

* SQL Injection (Intval)
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#sql-injection

* Cross Site Scripting (XSS)
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#cross-site-scripting-xss<Paste>

* External file inclusion
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#cross-site-scripting-xss

* Integrity of external JavaScript files
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#integrity-of-external-javascript-files

* Risk of externally hosted JavaScript libraries
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#risk-of-externally-hosted-javascript-libraries

* Raw HTML in content elements
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#content-elements

--

* Security headers & https

???

* Know differenct of http and https (SSL)

* Clickjacking (X-Frame-Options)
  https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#clickjacking

* Content Security Policy
  https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy

--

* Global TYPO3 configuration options

???

See: https://docs.typo3.org/m/typo3/reference-coreapi/master/en-us/Security/GuidelinesIntegrators/Index.html#global-typo3-configuration-options

* trustedHostsPattern
* lockSSL
* displayErrors
* devIPmask
* cookieSecure
* warning_email_addr / warning_mode
* fileDenyPattern
* lockIP / lockIPv6, enabledBeUserIPLock, IPmaskList

--

* Backup strategy

???

* Have a way to automatically create backup of database and filesystem.
* Also have a way to restore data for fielsystem and database.

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
