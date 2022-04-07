---
type: MUST
id: R000029
---

# prepare consumers to accept compatible API extensions

Service consumers should apply the robustness principle:

- Be conservative with API inputs and avoid exploiting definition deficits. For example do not pass megabytes of content for an input string that has no defined maximum length.
- Be tolerant in processing and reading data of API outputs.

More specifically service consumers must be prepared for compatible API extensions of service providers:

- Be tolerant with unknown fields in the payload (see also Martin Fowler’s post about ["TolerantReader"](http://martinfowler.com/bliki/TolerantReader.html)).
- Be prepared that `x-extensible-enum` output types may deliver new values; either be agnostic or provide default behavior for unknown values (see [SHOULD use extensible enums](@guidelines/R000035)).