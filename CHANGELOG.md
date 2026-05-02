# Changelog

All notable changes to the TailScale_deploy project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-05-02
### Added
- Pre-run check for any stale apt locks

### Fixed
- Semaphore jobs getting stuck in `Running` state due to docker updates
  - If any docker updates are pending, they will be put on hold and the playbook will proceed with patching. 
      Once the playbook finishes, the docker updates will be unheld and can be installed in a separate job or manually.

---

## Legend

- **Added** - New features
- **Changed** - Changes to existing functionality
- **Deprecated** - Soon-to-be removed features
- **Removed** - Removed features
- **Fixed** - Bug fixes
- **Security** - Security vulnerability fixes
