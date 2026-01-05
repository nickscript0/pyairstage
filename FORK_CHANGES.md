# Fork Changes

This is a fork of [danielkaldheim/pyairstage](https://github.com/danielkaldheim/pyairstage), forked from version 2.4.3 (commit `61c2fba`).

## Summary

This fork adds US region support, defrost mode detection, and improved error logging for the pyairstage library.

## Changelog

### [2025-11-24] - Defrost Mode Support
- **move get_defrost_status to proper module** (`b59140c`)
  - Moved `get_defrost_status()` method from `airstageApi.py` to `airstageAC.py`
  
- **improve warning** (`e022a04`)
  - Enhanced warning message for unexpected defrost mode values

- **Add defrost mode parameter (iu_op_stat) with getter method and validation logging** (`924b98a`)
  - Added `DEFROST_MODE` parameter to constants
  - Implemented `get_defrost_status()` method to detect defrost cycle status
  - Added validation logging for unexpected values

### [2025-11-23] - US Region & Error Logging
- **add us region support, copying eu auth path** (`abbead1`)
  - Added support for US region API endpoint (`bke.us.airstagelight.com`)
  - Updated region validation error messages

- **Log full HTTP response status and body on API errors** (`7c38a81`)
  - Improved error logging to include HTTP status code and response body
  - Better error handling for non-200 responses
