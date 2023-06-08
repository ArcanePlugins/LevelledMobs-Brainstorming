# Release

- `v4.0.0`
    - "After nine years in development, hopefully it'll be worth the wait." Gabe Newell

- `v4.0.1`
    - Fixed a logic error in custom drops parsing.

- `v4.1.0`
    - Added various integrations with third-party plugins.

- `v5.0.0`
    - Plugin is now rewritten in x86 Assembly.
    - A port to AArch64/ARM64 Assembly will soon follow!

# Release Candidates

*(aka Snapshots, Dev Builds)*

- `v4.0.0-alpha1` (initial version)
    - Welcome, testers and users, to the first test-ready build of LM4.
- `v4.0.0-alpha2` (update but still likely unstable)
    - Improved the reliability of mob label packets.
- `v4.0.1-beta1` (mostly stable, just needs a bit more testing to release)
    - Fixed part of the logic error in custom drops parsing.

# Differences with Semantic Versioning

In the `major.minor.patch` version format, SemVer increments the `major` version when a breaking API change has been made.

However, LM4 will use the `major` version instead as a 'revamp' version, i.e., how LM1-4 are majorly different from each other (internally and/or externally). 

# Synchronisation

ALL LevelledMobs source code modules share the same version. This includes API modules, plugin modules, etc. For convenience, the parent module will only use the major version as an integer (i.e., `4`), this doesn't matter to users or developers anyhow, just a way to make it easier for Maven to resolve the project structure.

This has the advantage of knowing which version is the latest for any given module as they all share the same string, however it does mean that modules will receive updates with 'no changes'. This doesn't really matter much, as it strongly outweighs the alternative.
