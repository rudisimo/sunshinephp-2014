# SunshinePHP 2014

## Day 1: Tutorials

### Code Review for Security

> By [Anthony Ferrara][1]

#### Notes

* Do not allow XML input from the user.
* X-Frame-Options: prevents click-jacking.
* Strict-Transport-Security: enforces SSL.
* **PLEASE**, don't use WordPress.

#### Encryption

* bcrypt
* scrypt
* pbkdf2
* PHPASS

#### Links

* [Security Quiz][3]
* [XSS (Cross Site Scripting) Prevention Cheat Sheet][4]
* [Essential PHP Security][5] by Chris Shiflett
* [Survive The Deep End: PHP Security][6]


### ZF2 Modules Workshop

> By [Evan Coury][2]

#### Intro to ZF2

* ZF2: It's good
* ZF3: It's better
* ZF2: Key Features
  * Zend\ModuleManager: everything is a module
  * Zend\ServiceManager: inversion of control / dependency injection
  * Zend\EventManager: completely event-driven
* [Zend Developer Tools][7]
* Modules can be anything!
  * Plugins
  * Themes
  * Libraries
  * Applications

---

[1]: https://twitter.com/ircmaxell
[2]: https://twitter.com/evandotpro
[3]: http://bit.ly/sec-quiz
[4]: https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet
[5]: http://phpsecurity.org/
[6]: http://phpsecurity.readthedocs.org/en/latest/
[7]: https://github.com/zendframework/ZendDeveloperTools