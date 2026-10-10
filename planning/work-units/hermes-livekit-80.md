# Current Hermes runtime compatibility

Issue: https://github.com/kortexa-ai/hermes-livekit/issues/80

Support managed Python 3.14 without changing the verified runtime dependency
pins. Keep the pip distribution available and add a native directory plugin
under `hermes_livekit/`. Its metadata-only dependency project lets Hermes PM
resolve the same plugin for independent profiles in one shared environment.
Use the normal plugin installer and gateway lifecycle for deployment.

Validate public adapter and registration contracts against current vanilla
Hermes and `kortexa-ai/main`. Test directory discovery and PM membership for
two profiles, then verify both Snappy profiles with real transport canaries.
Preserve profile credentials, selected models, and unrelated running work.
Record exact revisions, test results, deployment, and recovery evidence in the
issue. Do not place live execution status in this contract.
