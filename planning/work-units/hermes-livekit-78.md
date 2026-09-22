# Generic outbound phone configuration guide

Work unit: <https://github.com/kortexa-ai/hermes-livekit/issues/78>

## Contract

Document Twilio Elastic SIP Trunking and LiveKit Cloud configuration for
outbound phone calls, with an implementation design for Hermes Agent through
hermes-livekit. Keep account values and inference providers generic. Separate
usable external-service configuration from proposed plugin interfaces.

The guide covers credential boundaries, TLS/SRTP, caller IDs, destination
permissions, controlled audio tests, current fixed-room adapter limitations,
call ownership, readiness, authorization, media, deadlines, cleanup,
recovery, diagnostics, and acceptance criteria. Link it from the README.

This work changes documentation only. It does not implement dialing, modify
cloud accounts, change profile defaults, or place a test call.

## Verification approach

Read current primary vendor documentation and the existing plugin source.
Validate JSON and Python examples against the installed SDK without network
side effects. Check local links and anchors, placeholder usage, and the final
diff. Keep delivery receipts in the issue rather than these shipped bytes.

## Validation evidence

Two JSON examples parsed against the installed LiveKit protobuf schemas;
the proposed YAML parsed with outbound calling disabled. Both Python examples
executed with fake API clients and dummy credentials, without network calls.
All 19 local links and anchors resolved. Placeholder checks found only the
two fictional telephone numbers and no deployment-specific configuration.
`git diff --check` passed. CLI help and SDK source checks covered the shown
operations, method timeout, and explicit suppression of request failover.

No live carrier call or service reconfiguration was needed for this document.
