# Boldly going where no F# has gone before - Alexa skills in F#

Aim: Alexa, Fable

## Journey
- F# dev
- Jan, moved: JS, Alexa

## Primer on Alexa

- Overview
- Crappy Architecture Diagram
- Requests (+ slots)
- Response

## SDKs

- Bad: emit, magic strings, copy/paste docs.
- Used it for a bit.
- TS
- F#: Core, Team, Learn, Fable

## F#

- Domain modelling
- Fable: No examples of lambda
  - System.Func
  - Async



- Built first skill, SDK sucked
- Built alexa-ts as better version of SDK
- Problems:
  - Still not that safe
  - Quite verbose.
  - Still looks like JavaScript :P
- Limitations:
  - Only using AWS in production.
  - Alexa pushes the Lambda route.

But that's okay because AWS Lambda supports .net core right?
- Built a demo
- Start up time too slow to respond before Alexa got bored :(

Not all is lost ... Fable to the rescue!
- Not used it before, but seen a couple of post about it.
- A few references about using it with node+express.
- Nothing on Lambdas
- How hard can it be?
- Aim build a minimal, non-abstracted library.

## Primer on Alexa
- Skill = app for voice
- Invocation name = identify your skill
- Wake word = start listening
- Intent = method
  - Speech -> Intent is figured out by Amazon through provided examples.

## Domain model
- Request types
- Response:
  - Say (+ reprompt?)
  - Card
  - End?
- Session (+ attributes)
- Bootstrapper

## Interop
Learning F#<>JS interop
- POJO
- StringEnum
- Emit (jsNative)
- Dynamic props
- Partial application -> System.Func<_,_,_,_>
- Async -> callbacks

## F# vs TypeScript
- Interfaces vs Records
- Inference - how it fails
