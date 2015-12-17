# Event Loop Meta Document

## 1. Summary

The purpose of this proposal is to provide a common interface for event loop
implementations. This will allow libraries and components from different
vendors to operate in an event driven architecture, sharing a common event
loop.

## 2. Why Bother?

Some programming languages, such as Javascript, have an event loop that is
native to the execution environment. This allows package vendors to easily
create asynchronous software that uses this native event loop. Although PHP
is historically a synchronous programming environment, it is still possible
to use asynchronous programming techniques. Using these techniques, package
vendors have created PHP event loop implementations that have seen success.

However, as these event loop implementations are from package vendors, it
is not yet possible to create event driven software components that are
independent of the underlying event loop implementation. By creating a
common interface for an event loop, interoperability of this nature will
be possible.

## 3. Scope

## 3.1 Goals

The functionality exposed by this interface should include the ability to:

- Watch input streams for available data
- Watch output streams for the ability to perform non-blocking write operations
- Run single and periodic timers
- Listen for signals
- Defer execution

## 4. People

### 4.1 Editors

* [Andrew Carter](https://github.com/AndrewCarterUK)
* [Cees-Jan Kiewiet](https://github.com/WyriHaximus)

### 4.2 Sponsors

* [Aaron Piotrowski](https://github.com/trowski) (Coordinator)
* [Christopher Pitt](https://github.com/assertchris)
