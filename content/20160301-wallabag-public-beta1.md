date: 2016-03-01 08:00:00+00:00
slug: wallabag-public-beta1
title: First public beta for wallabag v2
tags: v2

Last week, [we published our roadmap]({filename}/20160220-roadmap-wallabag-v2.md) for this year:
* wallabag v2.0.0-beta.1 on 1st March
* wallabag v2.0.0 on 3rd April
* wallabag v2.2.0 on 3rd October

And do you know what? **We are on 1st March**. So, it's the **beta day**!

## wallabag v2.0.0-beta.1

If you missed our recent blog posts, here are the main features of wallabag v2:

* a REST API ([you can have a look to the documentation](http://v2.wallabag.org/api/doc))
* authorization via oAuth2
* a new default theme, called `material`
* save an article, read it, favorite it, archive it. (Hopefully)
* annotations: In each article you read, you can write annotations. ([read the doc](http://doc.wallabag.org/en/v2/user/annotations.html))
* assign tags to entries
* edit article titles
* RSS feeds (with ability to limit number of articles)
* create a new account from the config page
* filter entries by reading time, domain name, creation date, status, etc.
* recover passwords from login page (you have to fill your email on config page)
* picture preview, if available, is displayed for each entry
* Public registration
* migration from wallabag v1/v2 (based on JSON export) ([read the doc](http://doc.wallabag.org/en/v2/user/import.html))
* migration from Pocket (it works, but we need to implement asynchronous import: if you have too many articles, it can fail) ([read the doc](http://doc.wallabag.org/en/v2/user/import.html))
* exports in many formats (PDF, JSON, EPUB, MOBI, XML, CSV and TXT).
* 2-Factor authentication via email ([read the doc](http://doc.wallabag.org/en/v2/user/configuration.html#two-factor-authentication))
* Tagging rule: create a rule to automatically assign tags to entries! ([read the doc](http://doc.wallabag.org/en/v2/user/configuration.html#tagging-rules))
* German, French, Turkish, Persian, Romanian, Polish, Danish and English translations
* Added Quickstart for beginners (when you don't have any entries)
* maintenance mode (useful when you'll upgrade your wallabag platform)
* Internal settings for Administrator (the account created during installation). We need to documentate this part of wallabag.

We have work to do on our API, [you can have a look on this pull request](https://github.com/wallabag/wallabag/pull/1675).

### What's new since last alpha?

The big feature is the annotations. [Thank you Thomas](https://github.com/tcitworld))!

### Documentation

v2 documentation is already available (we still need to write some chapters), you can read it here: http://doc.wallabag.org

Our documentation is now hosted on [ReadTheDocs](http://readthedocs.org/).

### Translate wallabag and documentation

Please read this page: [http://doc.wallabag.org/en/v2/developer/translate.html](http://doc.wallabag.org/en/v2/developer/translate.html).

### Third-party applications

Our applications (Firefox / Chrome addons and Android / iOS / Windows Phone) are not available for wallabag v2 but we'll work on them to change that.

## Test wallabag

### On a dedicated web server

Keep in mind it's an **unstable** branch, everything can be broken :)

If you don't have it yet, please [install composer](https://getcomposer.org/download/). Then you can install wallabag by executing the following commands:

```
SYMFONY_ENV=prod composer create-project wallabag/wallabag wallabag "2.0.*@beta" --no-dev
php bin/console wallabag:install --env=prod
php bin/console server:run --env=prod
```

### On our demo platform

We published this version on [http://v2.wallabag.org](http://v2.wallabag.org) but please remind it's just a demo platform and we can drop database at any time.

You can create a free account on this platform.

## How can you help us?

Test, test and test! Install wallabag v2 (see above `On a dedicated web server` chapter) and tell us if you have any problems.

Don't forget that [you can also support us via Paypal, Flattr, Gratipay or Bountysource](https://www.wallabag.org/pages/donations.html).

## What's next?

We planned to released stable version on 3rd April. In one month. We have lot of work to release this version ([see here our todo list](https://github.com/wallabag/wallabag/milestones/2.0.0)). Maybe we'll release other betas before this deadline.

We need help, feel free to contribute to this great project!
