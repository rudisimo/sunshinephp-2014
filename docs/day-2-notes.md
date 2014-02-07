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



## Profiling PHP with XHProf

> By [Jonathan Klein][4]



## Decoupled CMS

> By [Lukas Kahwe Smith][5]



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