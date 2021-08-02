Changes to the `ini` package
=====

v0.5
-----

The behavior of `(<>)` and `mappend` for the `Ini` type has changed.

  * `<>` previously discarded all `iniGlobals`. Now it concatenates
    the globals from the two `Ini` values.

  * When two `Ini` values contained `iniSections` with the same name,
    `<>` previously returned the section from the left value and
    discarded the section of the same name from the right value.
    Now it concatenates the sections of the same name.
