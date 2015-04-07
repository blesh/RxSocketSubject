- 0.6.3
  - Update rxjs and rx-dom dependencies
- 0.6.2
	- BUGFIX: Remove leftover debug statement
- 0.6.1
  - BUGFIX: Ensure underlying socket reconnects when new connection information provided
- 0.6.0
	- BREAKING: multiplex `responseFilter` argument moved to `config` parameter. Signature changed.
	- FEATURE: Add optional per-multiplexer responseFilter argument. This allows for more granular control of response identification. Default can be used, then multiplexer responseFilter argument can override.
- 0.5.0
	- FEATURE: Add `multiplex` method to RxSocketSubject. Multiplex is a new method that returns a function with which Observables can be created that multiplex data over the underlying RxSocketSubject.
	- FEATURE: Add `serializer` and `deserializer` configuration properties to multiplexing. Allows for custom serialization.
	- FEATURE: Add `subscriberProxy` to multiplex configuration. Allows for custom pre-processing of subscription and unsubscription messages prior to being serialized and sent over the socket.
	- FEATURE: Add `messageProxy` to multiplex configuration. Allows for custom processing of raw socket message events prior to deserialization. Useful for things like batching responses.
- 0.4.0
	- REFACTOR: Move RxSocketSubject over to being a custom class extending AnonymousSubject