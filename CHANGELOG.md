# Version 1.3.0

This release brings minor changes to snapshot testing by adding an additional option to remove version headers from generated code. This will make our snapshot tests more robust by preventing test breakage that used to occur when updating our version.

* `typeshare-core`
  * Each language implementation now has an additional public variable that can be set to remove version headers from generated code.

# Version 1.2.0

This release brings Scala functionality to the CLI, support for Apple Silicon as a pre-built binary, and refactors how
we handle language variants internally to be more type-safe.

* `typeshare-cli`
  * Scala is now a language generation target! Try it out with `typeshare --lang=scala --scala-package=com.your.package.here some/file.rs`
  * Future releases (including this one) now support aarch64-apple-darwin as an additional architecture.
* `typeshare-core`
  * Language variants are now represented as enums instead of strings.

### Community contributors

Thank you to the following community contributors for your work on this release:
* [jclmnop](https://github.com/jclmnop)
* [oeb25](https://github.com/oeb25)
* [DuhPesky](https://github.com/DuhPesky)
* [exoego](https://github.com/exoego)

# Version 1.1.0

This release brings major new additions, the largest of which is support for Scala as a language generation target. 
Additionally, the code generation API has been expanded/revised, and many bugs have been fixed.

* `typeshare-cli`
  * Kotlin now uses `val` consistently for defining fields.
  * Some issues with the command line options have been corrected.
  * Unit structs that don't use bracket syntax are now supported.
  * Typescript can now handle type aliases of optional types.
  * Empty structs are now represented as objects in Kotlin.
  * You can now define read-only Typescript properties with `#[typeshare(typescript(readonly))]`.
  * Doubly-nested option types (`Option<Option<T>>`) are now supported in Typescript.

* `typeshare-core`
  * The `Language` trait now takes `self` mutably for more flexibility in implementations.
  * Scala is now a supported language for code generation, though the CLI does not use it yet.
  * The attribute parser has been reworked to be more robust and flexible for future additions.

* Miscellaneous
  * We now have a proper release system and prebuilt binaries for anyone to download 🎉
  * Releases will be weekly on every Thursday.

### Community Contributors
Thank you to the following community contributors for your work on this release:

[exoego](https://github.com/exoego), [Czocher](https://github.com/Czocher), [ccouzens](https://github.com/ccouzens),
[McAJBen](https://github.com/McAJBen), [adriangb](https://github.com/adriangb), [kareid](https://github.com/kareid),
[nihaals](https://github.com/nihaals), [ChrisMcKenzie](https://github.com/ChrisMcKenzie), [justintime4tea](https://github.com/justintime4tea),
[prestontw](https://github.com/prestontw), and [julienfouilhe](https://github.com/julienfouilhe)!
