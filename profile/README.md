## Hi there 👋

### How it started

@xrobau:
```
The provably anonymous voting 'stuff' I have currently done is pretty simple. Basically
you have service A generate a bunch of random tokens. These are returned to service B.
Service B mixes them, and a bunch of email addresses together, and then hands that to
service C which actually emails them. The tokens are basically JWTs.

The rx'ing instance validates the JWT, marks it as used, and records the vote.

the reason you use JWTs is that you don't need to have the generation and validation service
talk to each other at all. The JWT says 'valid for xyz, uuid foo'. The validation service
checks that it's being used for xyz and that uuid foo hasn't already responded.
```

