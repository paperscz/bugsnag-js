- [ ] Configuration of external plugins, consistency?
- [ ] Ensure `noConflict()` is not necessary and/or document how to instantiate multiple clients in the same environment
- [ ] In v4 implementation of `notify()` warn of deprecated `notifyException(string, string)` usage. Attach arguments as `metaData`.
- [ ] In v4 implementation of `notify(err, opts)` coerce null -> {}
- [ ] Refer to Ruby upgrade guide for example on changing `notify()` usage
- [ ] Augment `BugsnagReport.ensureReport()` to account for objects like the jQuery error event, and any other obvious/pertinent examples
- [ ] Merge the inline script PR
- [ ] Chain existing window.onerror function
- [ ] Make a low priority task to test stacktrace logic cross browser
- [ ] Ensure opts passed to notify() merge with sensible precedence
- [ ] Deal with CORS script error things https://docs.bugsnag.com/platforms/browsers/faq/#3-cross-origin-script-errors
- [ ] Test bad user input for unhandled rejection plugin
- [ ] Logging. Do we/don't we?

- [x] Check the length of the stringified payload (limit 1MB)
- [x] Ensure breadcrumb limit can be set to 0
- [x] Reorder `leaveBreadcrumb()` arguments: `name` `metaData`, `type`, `timestamp`
- [x] Ensure only valid-shaped breadcrumbs get recorded
- [x] Ensure no duplicates in breadcrumbs
- [x] Only leaveBreadcrumb() for errors if it actually sent