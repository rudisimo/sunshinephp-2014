# Day 2: Talks

## Development, By The Numbers

> By [Anthony Ferrara][1]

* The central enemy of reliability is complexity.
* Cyclomatic Complexity:
  * Single Method: 11+ (Very High)
  * Average Per Method: 6+ (Very High)
  * Average Per Line of Code: 15+ (Very High)
* NPath Complexity:
  * Threshold: 200
* NPath helps identify how many Unit Tests should be written.
* Change Risk Analysis Procedure (C.R.A.P.)
* Useful Tools:
  * PHPLOC: Summarizes an entire codebase
  * PDepend: Lower Level analysis
  * PHPMD: Finds messy code
  * [Sonar][6]: Like Jenkins (with a tighter integration)
  * [Splunk][7]: Helps you understand your data
* No single tool has the answer; together they help paint the bigger picture. Make your decisions based on that.

## Building Testable PHP Applications

> By [Chris Hartjes][2]

* Chris swears **A LOT**.
* Onion Architecture:
  * Organize the layers of your application code like the layers of an onion.
  * Every layer of the onion is only coupled or dependent upon any layer deeper in the onion.
* Hoare's Law of Large Programs:
  * Inside every large program is a small program struggling to get out.
* Your framework should be an implementation detail, not a giant killer squid, sucking the life out of your application.
* [The Law of Demeter][8]
* Thins to Mock:
  * Databases
  * APIs
* Mocking Tools:
  * PHPUnit's built-in support
  * [Mockery][9]
  * [Prophecy][10]
* [Etsy's PHPUnit Extensions][11]
* Databases: always mock, relying on a database belongs to an Integration Test, not a Unit Test.
* Your app shouldn't care what environment it runs in.
* [PHPDotEnv][12]: Loads environmental variables automagically.
* Books:
  * [The Grumpy Programmer's PHPUnit Cookbook][13]
  * [The Grumpy Programmer's Guide To Building Testable PHP Applications][14]

## Application Logic Security

> By [Ilia Alshanetsky][3]

* OWASP Top 10 List (Review)

### Authentication

* Enforce password rules
* Use `/dev/urandom` for randomness.
* PHP 5.5 makes password hashing extremely easy.
* Limit number of sequential unsuccessful requests to 3-5.
  * Use CAPTCHA.
  * Multi-factor authentication.
  * Lock account for 10-15 minutes.
  * Implement IP address blocks (be very careful).
* Don't use the typical field names (login, password, username), randomize them with a session salt instead.
* Tie user sessions to IP address and/or browser.
* Enforce low session expiry times.
* Idle time logout after 10 minutes of inactivity.
* Require re-authentication for profile changes and/or e-commerce activities.
* Prevent duplicate logins.
* Use proper security headers:
  * X-Frame-Options: DENY
  * Strict-Transport-Security
* Do not use the GET method to make requests (including Ajax).

### Session Security

* Use only cookies
* Ensure session ID integrity
  * Change entropy file to `/dev/urandom` and increase the entropy size.
* Use HTTPOnly cookies for sessions storage
* Set Secure session bit (SSL/TLS)
* Approach ACL with a whitelist, not blacklist method.
* Audit user activity, look for patterns of unusual activity.

## Profiling PHP with XHProf

> By [Jonathan Klein][4]

* [XHGui][15]
* Workflow:
  * Run XHProf
  * Find expensive functions
  * Instrument with StatsD (optional)
  * Optimize
* Pro Tips:
  * Sort by number of calls
  * Look for multiples of 40
  * Turn off CPU measurement (save overhead)
  * Call graphs
  * Enable via query string parameter (on demand)
* Takeaways
  * Profiling is easy
  * You get what you measure

## Decoupled CMS

> By [Lukas Kahwe Smith][5]

* [prose.io][16]: content editor for Github

[1]: https://twitter.com/ircmaxell
[2]: https://twitter.com/grmpyprogrammer
[3]: https://twitter.com/iliaa
[4]: https://twitter.com/jonathanklein
[5]: https://twitter.com/lsmith
[6]: http://www.sonarsource.com/products/editions/
[7]: http://dev.splunk.com/
[8]: http://en.wikipedia.org/wiki/Law_of_Demeter
[9]: https://github.com/padraic/mockery
[10]: https://github.com/phpspec/prophecy
[11]: https://github.com/etsy/phpunit-extensions
[12]: https://github.com/vlucas/phpdotenv
[13]: https://leanpub.com/grumpy-phpunit
[14]: https://leanpub.com/grumpy-testing
[15]: https://github.com/perftools/xhgui
[16]: http://prose.io/