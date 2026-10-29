# Changelog

## Unreleased

- Moved to its own repository, github.com/pyxpo/pyxpo-translate, with CI on Python 3.9 and 3.12 and releases from tags.
- Added a security policy, a contributing guide and issue templates.

## 0.1.0a1

- First release: offline text translation on Android with Google ML Kit's on-device models. `download_async`
  fetches one language's model (about 30 MB, optionally on Wi-Fi only); `translate_async` then runs on the phone
  and refuses a language that is not downloaded instead of fetching it. `status_async`, `downloaded_async`,
  `is_ready_async`, `languages_async`, `delete_async` and `close_async` manage the models. Text is never sent or
  logged. Works headless, so a `pyxpo-keyboard` input method can call it. iOS, the web and the desktop raise
  `NotSupportedError`.
