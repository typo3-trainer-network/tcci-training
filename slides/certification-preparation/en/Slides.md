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
name: introduction
class: center, middle, h1-fullwidth
layout: false

# Introduction
---
name: introductionx
class: h1-fullwidth
# Introduction

* 
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

* Web server
???
* know is possible on most current versions such apache, nginx or iis
* understand about mod-rewrite, htaccess 
* know about SSL support

--

* PHP (Versions, Modules, Settings)
???
* version 10 from PHP >= 7.2 <= 7.4
* you know where to find information about incompatibilities and new features http://php.net/manual/en/migration70.php
* you know about basic modules you need like zip, pdo, mysqli, openssl, etc

--

* DBMS
???
* know about Doctrine
* version 10 from MySQL >= 5 <= 5.7, Postgres, SQL, SQLite or MariaDB >= 10 <= 10.3
* know about data base privileges

--

* Image processing
???
* know where temporary data is stored (typo3temp)
* know where you can configure and test the processor (Install tool: Environment)

--

* Commandline commands
???
* know how to use composer for installing distribution, extensions and updates
* know how to use cli commands for updating languages, run cron jobs, block installations

--

* Operating systems
???
* know that it should run on any OS if it has a web server for PHP and database server

--

* Web browsers
???
* know that the backend is not supported for most versions of Internet Explorer, only Edge

---
name: installways
class: h1-fullwidth
# Installation guide

* get.typo3.org
    * composer
    * git
    * direct downloads

???
* know how to download the distribution package using composer, this is the recommended way 
See: https://docs.typo3.org/m/typo3/guide-installation/master/en-us/QuickInstall/Composer/Index.html
* or creating a composer.json file including the necessary system extensions using the composer helper
See: https://get.typo3.org/misc/composer/helper
* know how to download the source from Git git clone
See: https://github.com/TYPO3/TYPO3.CMS
* know also how to download the source package distribution using wget, curl or direct download
* know that when using composer mode the Extension Manager can not be used for installing, removing or updating extensions

--

* Distributions
???
* know that a distribution is a preconfigured installation
* know that it is possible to select a predefined distribution on a first time installation
--

* Root level folders and file structure
???
* public:is the document root and public entry point
* var: contains system files, like caches, logs, sessions…
* vendor: contains third-party php packages, libraries etc.
---
name: installtypo3
class: h1-fullwidth
# TYPO3 Tools

* Install tool
???
* know that it is used to configure the system not just for installing it
* know that it is located in typo3/install
* on the frontend it can be accessed as http://www.example.com/typo3/install.php
if the file ENABLE_INSTALL_TOOL exists under typo3conf/
* on the backend it can be accessed by System Maintainers only under the Admin Tools module
```php
TYPO3_CONF_VARS[SYS][systemMaintainers] = '';
```

--
 
* Step wizard
???
* create the FIRST_INSTALL file in the document root
* know how to fix system environment issues
See: https://docs.typo3.org/m/typo3/guide-installation/master/en-us/Troubleshooting/Index.html#troubleshooting
* know that  the database connection information is set here the first time to use or create a new database
* know that the password for the administrator user and install tool are configured here the first time
--

* Password handling
???
* there are not default passwords for protected areas
* first created administrator has the same password as the install tool which must be changed right after installation
* there is at the moment no option for recovering passwords
* from the install tool it is only possible to create a new administrator user
* if having access to the database a new password can be used to replace the previous one
The new password can be generated using the php command password_hash() for the configured encryption method

--

* Upgrade functions
    * Core upgrade
    * Upgrade wizard

???
* know that there is a Core Upgrade function that can be uses for maintenance and bugfixes releases , it works if:
tar is available on ser server
the setup uses symbolic links
the symbolic links, the web root and the above path directory have the right permissions by the web server
* know that there is an Upgrade wizard function that must be used after a major release upgrade,
* know how to check status of the database and perform updates on table and fields structure using

--

* Translating the Backend
???
* know that the Manage Language Packs option can be found on the Maintenance module and it used todownload the translations of the available extensions which includes the backend system extensions for the chosen languages

---
name: typo3console
class: h1-fullwidth

# TYPO3 Console

* install packages and distributions

```php
composer create-project "typo3/cms-base-distribution:^10" my-new-project
```

* perform site and system tasks

```php
php .vendor/bin/typo3 language:update
```
```php
php .vendor/bin/typo3cms cache:flush --force
```

* available commands

```php
php public/typo3/sysext/core/bin/typo3 list
```

???
* know that you can use an external extension for commands based on the Symfony Console
* know how you can find the list of available commands for the Command Line Inter- face module dispatcher
updating language packages
update reference index
flush caching
site configuration information
lock / unlock backend
etc


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
