# LR1121 modem driver changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-07-02

### Added

- `lr1121_modem_system_get_status_and_clear_reset_source` that replaces `lr1121_modem_system_clear_reset_status_info` and `lr1121_modem_system_get_status`
- Documentation of Tx Done status `lr1121_modem_tx_done_event_t`

### Fixed

- `lr1121_modem_system_set_dio_irq_params` was disabling an internal IRQ
- Implementation of `lr1121_modem_system_get_irq_status` to not rely on HAL function `lr1121_modem_hal_direct_read`
- Documentation of `lr1121_modem_get_next_tx_max_payload`
- Various conversion, sign-conversion, switch default, and unused macros compilation warnings

### Changed

- `lr1121_modem_system_set_sleep` can configure sleep mode without RTC running

### Removed

- `lr1121_modem_hal_direct_read` from Modem HAL API
- `lr1121_modem_system_clear_reset_status_info` and `lr1121_modem_system_get_status` which are replaced by `lr1121_modem_system_get_status_and_clear_reset_source`

## [v1.0.0] - 2024-09-19

- Initial release
