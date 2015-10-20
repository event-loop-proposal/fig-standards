# Event Loop Meta Document

## 1. Summary

The purpose of this proposal is to provide a common interface for event loop
implementations.

For PHP libraries and components from separate vendors to operate in an event
driven architecture, they must share a common event loop. This event loop could
be used to poll input/output streams, defer execution, operate timers and
handle signals.
