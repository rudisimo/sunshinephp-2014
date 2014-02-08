# Day 3: Talks

## Keynote: Open Source, PHP, and PIE

> By [Larry Garfield][9]

* [PHP-FIG][10]: PHP Framework Interoperability Group
* [Guzzle][6]: HTTP client and framework for RESTful web services.
* [EasyRDF][7]: Library for consuming and producing RDF.
* [Zend Feed][8]: Library for consuming and producing RSS/Atom feeds.

## Modern PHP

> By [Ben Ramsey][1]

...

## Building better developers

> By [Rowan Merewood][2]

* Reading Material
  * Code Kata – Dave Thomas
  * TDD Kata – Roy Osherove
* Levels of Proficiency
  * Novice
  * Beginner
  * Competent
  * Proficient
  * Expert
* Measure systems, don't measure people (they'll just mess it up)

## Keynote: APIs: Dead Reckoning

> By [Matthew Weier O'Phinney][11]

* Filter input, escape output
* Hypermedia Application Language (HAL)
* Problem Details for HTTP APIs
* Use OPTIONS method
* [apigility][12]

## UA Testing with Selenium and PHPUnit

> By [Michelangelo Van Dam][3]

...

## Vagrant, Puppet and Chef FTW

> By [Thijs Feryn][4]

* One environment per project
* Dev ~= Test ~= Staging ~= Prod
* Easy to define & transport
* Easy to tear down
* Provisionable: infrastructure as code
* Versionable
* Shared across the team
* Provisioning
  * Shell
  * [Ansible][13]
  * Chef Solo
  * Chef Client
  * Puppet Apply
  * Puppet Agent
* Create ramdisk for caching
* Chef it is!

## Redis Everywhere

> By [Ricard Clau][5]

* **RE**mote **DI**ctionary **S**erver
* Data Types
  * Strings up to 512 MB
  * Lists of elements sorted by insertion order
  * Sets unordered collection of elements supporting unions, intersections and differences
  * Hashes key-value pairs
  * Sorted sets automatically ordered by score
* It has configurable persistence
  * RDB snapshots
  * AOF persistence logs
  * Combination of both, or no persistence at all
* *"Memory is the new disk, disk is the new tape"*
* Features
  * Master/slave replication
  * Pipelining to improve performance
  * Transactions
  * Pub/Sub pattern
  * Scripting with LUA (~sorted procedures)
  * Predictable performance (check commands complexity)
* Hardware Tips
  * Single-threaded, so a 2 core machine is enough
  * CPU is rarely the bottleneck
* [redis.io/commands][14]: Test commands straight from your browser
* [SncRedisBundle][15]: Symfony2 bundle for Redis
* Redis as a Queue
  * Using Lists and LPUSH/RPOP instructions
  * Send OpenGraph requests to Facebook with Python daemons
  * Use RabbitMQ for advanced message queuing features
* Uses
  * System statistics dashboard
  * Leaderboards
  * Who is online?
    *     
  * Friends online?
    * SINTERSTORE "friends-<userid>-online"
* Distributed Locking
  * SET <lock> I NX EX <seconds>
* [aphyr.com][16]

[1]: https://twitter.com/ramsey
[2]: https://twitter.com/rowan_m‎
[3]: https://twitter.com/DragonBe
[4]: https://twitter.com/ThijsFeryn
[5]: https://twitter.com/ricardclau
[6]: https://github.com/guzzle/guzzle
[7]: https://github.com/njh/easyrdf
[8]: http://framework.zend.com/manual/2.2/en/modules/zend.feed.introduction.html
[9]: https://twitter.com/Crell
[10]: https://github.com/php-fig/fig-standards
[11]: https://twitter.com/mwop
[12]: http://www.apigility.org
[13]: https://github.com/ansible/ansible
[14]: http://redis.io/commands
[15]: https://github.com/snc/SncRedisBundle
[16]: http://aphyr.com