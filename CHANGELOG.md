# Changelog

All notable changes to this project will be documented in this file. The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## UNRELEASED

## 1.5.1

### Changed

-   Metadata updates
-   Madhya Bihar Gramin Bank and Bihar Gramin Bank merged to form
    Dakshin Bihar Gramin Bank.

### Fixed

-   Fixes a critical bug in the node.js SDK which reported some valid IFSCs as invalid.
-   `CENTRE` and `CITY` fields should now be present across all rows. If we don't have a value, it will be set to `NA`.

### Added

-   New `DatasetTest` to ensure fields don't get missed out in the future

## 1.5.0

### Added

-   Adds bank constants in nodejs
-   Adds offline bank details fetch method in ruby.
-   Adds support for `upi: true` flag in `banks.json`
-   Adds `UPI: true/false` flag in `IFSC.csv` and `by-banks` JSON files

### Changed

-   Improves coverage of bank constants in ruby.

## [1.4.10][1.4.10] - 2020-01-02

-   Metadata Updates
-   Support for patches that can override data for specific IFSC codes
-   NEFT Block for certain banks:
    -   Bank Of Ceylon
    -   Krung Thai Bank
    -   Kaveri Grameena Bank
    -   Kerala Gramin Bank
    -   Pragathi Krishna Gramin Bank
    -   Sbm Bank Mauritius Ltd

## [1.4.9][1.4.8] - 2019-11-07

-   Metadata Updates

## [1.4.7][1.4.7] - 2019-10-14

-   Minor Metadata updates

## [1.4.6][1.4.6] - 2019-09-05

-   Metadata updates
-   Catholic Syrian Bank is renamed to CSB Bank

## [1.4.5][1.4.5] - 2019-07-15

-   Regular Metadata Updates

## [1.4.4][1.4.4] - 2019-06-17

### Changed

-   Regular Metadata Updates

### Added

-   Adds support for custom sublets. (#114)

## [1.4.2][1.4.2] - 2019-05-16

### Changed

-   Regular Metadata Updates

## [1.4.1][1.4.1] - 2019-04-25

### Fixed

-   Parsing of empty/NA MICR/IINs/IFSCs in NPCI ACH List. #100

### Changed

-   Updated list of sublets to remove all exceptions

## [1.4.0][1.4.0] - 2019-04-19

### Added

-   Regular Metadata Changes. See [Release Page][1.4.0] for a list.
-   One new Bank: `AJAR`
-   Adds NPCI-only IFSCs from https://www.npci.org.in/national-automated-clearing-live-members-1. See #100 and #109 for some more details.
-   A `NEFT=true|false` flag is added on all datasets, which will get added to the API with this release.
-   A `IMPS=true|false` flag is added, which is currently in alpha. There is not enough clarity around this yet (See #109), so please don't use this in production yet. This can be removed at any time. Feedback on the correctness of this flag is welcome.
-   A MICR is now available for all rows. This will also reflect on the API.

### Changed

-   Parser speed and general improvements. Builds only take 3 minutes, and caching related stuff is removed.
-   The parser converts XLS/XLSX files to CSV before parsing, which results in cleaner data in some cases.

### Removed

-   Removes some data formats (YAML/Large JSON) for cleaner code. If you were using them, please let create an issue.

[unreleased]: https://github.com/razorpay/ifsc/compare/1.4.9...HEAD
[1.4.10]: https://github.com/razorpay/ifsc/releases/tag/1.4.10
[1.4.9]: https://github.com/razorpay/ifsc/releases/tag/1.4.9
[1.4.8]: https://github.com/razorpay/ifsc/releases/tag/1.4.8
[1.4.7]: https://github.com/razorpay/ifsc/releases/tag/1.4.7
[1.4.6]: https://github.com/razorpay/ifsc/releases/tag/1.4.6
[1.4.5]: https://github.com/razorpay/ifsc/releases/tag/1.4.5
[1.4.4]: https://github.com/razorpay/ifsc/releases/tag/1.4.4
[1.4.3]: https://github.com/razorpay/ifsc/releases/tag/1.4.3
[1.4.2]: https://github.com/razorpay/ifsc/releases/tag/1.4.2
[1.4.1]: https://github.com/razorpay/ifsc/releases/tag/1.4.1
[1.3.4]: https://github.com/razorpay/ifsc/releases/tag/1.3.4
[1.3.3]: https://github.com/razorpay/ifsc/releases/tag/1.3.3
