Changelog
=========

FORK 2.0.0 (TBD)

* Move breaker state to enum

FORK 1.1.0 (Jan 14, 2019)

* Add logic to stop calling decorator trigger twice
* Fix bug with timeout window growing with additional breakers defined (Thanks @shawndrape)
* Remove threading support (unneeded with asyncio)

FORK 1.0.0 (Aug 12, 2018)

* Move over to asyncio
* Drop < 3.4 support
* Drop tornado support
* Async call support

Version 0.4.4 (May 21, 2018)

* Fix PyPI release

Version 0.4.3 (May 21, 2018)

* Re-initialize state on Redis if missing (Thanks @scascketta!)
* Add trigger exception into the CircuitBreakerError (Thanks @tczhaodachuan!)

Version 0.4.2 (November 9, 2017)

* Add optional name to CircuitBreaker (Thanks @chrisvaughn!)

Version 0.4.1 (October 2, 2017)

* Get initial CircuitBreaker state from state_storage (Thanks @alukach!)

Version 0.4.0 (June 23, 2017)

* Added optional support for asynchronous Tornado calls (Thanks @jeffrand!)
* Fixed typo (issue #19) (Thanks @jeffrand!)


Version 0.3.3 (June 2, 2017)

* Fixed bug that caused pybreaker to break (!) if redis package was not
  present (Thanks @phillbaker!)


Version 0.3.2 (June 1, 2017)

* Added support for optional Redis backing (Thanks @phillbaker!)
* Fixed: Should listener.failure be called when the circuit is closed
  and a call fails? (Thanks @sj175 for the report!)
* Fixed: Wrapped function is called twice during successful call in open
  state (Thanks @jstordeur!)


Version 0.3.1 (January 25, 2017)

* Added support for optional Redis backing


Version 0.3.0 (September 1, 2016)

* Fixed generator issue. (Thanks @dpdornseifer!)


Version 0.2.3 (July 25, 2014)

* Added support to generator functions. (Thanks @mauriciosl!)


Version 0.2.1 (October 23, 2010)

* Fixed a few concurrency bugs.


Version 0.2 (October 20, 2010)

* Several API changes, breaks backwards compatibility.
* New CircuitBreakerListener class that allows the user to listen to events in
  a circuit breaker without the need to subclass CircuitBreaker.
* Decorator now uses 'functools.wraps' to avoid loss of information on decorated
  functions.


Version 0.1.1 (October 17, 2010)

* Instance of CircuitBreaker can now be used as a decorator.
* Python 2.6+ is now required in order to make the same code base compatible
  with Python 3+.


Version 0.1 (October 16, 2010)

* First public release.
