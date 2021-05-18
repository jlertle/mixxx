# Mixxx
[![GitHub latest tag](https://img.shields.io/github/tag/mixxxdj/mixxx.svg)](https://mixxx.org/download)
[![Packaging status](https://repology.org/badge/tiny-repos/mixxx.svg)](https://repology.org/metapackage/mixxx/versions)
[![Zulip chat](https://img.shields.io/badge/zulip-join_chat-brightgreen.svg)](https://mixxx.zulipchat.com)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://mixxx.org/donate)

[Mixxx] is Free DJ software that gives you everything you need to perform live
DJ mixes. Mixxx works on GNU/Linux, Windows, and macOS.

## Quick Start

To get started with Mixxx:

1. For live use, [download the latest stable version][download-stable].
2. For experimentation and testing, [download a development release][download-testing].
3. To live on the bleeding edge, clone the repo: `git clone https://github.com/mixxxdj/mixxx.git`

## Bug tracker

The Mixxx team uses [Launchpad] to manage Mixxx development.

Have a bug or feature request? [File a bug on Launchpad][fileabug].

Want to get involved in Mixxx development? Assign yourself a bug from the [easy
bug list][easybugs] and get started!

## Compiling on Linux
    $ mkdir build
    $ cd build
    $ cmake ..
    $ cmake --build .
Please see our helpful guide on the [wiki] for more information: [Compiling on Linux]

## Compiling on MacOS
    $ mkdir build
    $ cd build
    $ cmake ..
    $ cmake --build .
Please see our helpful guide on the [wiki] for more information: [Compiling on MacOS]

## Compiling on Windows
### Build Requirements
- Windows 7 or later
- MS Visual Studio 2019 (Community Edition is free of charge)
- At least 10G free diskspace
- To create an .msi installer, you need to install the WiX toolkit from https://wixtoolset.org/releases/
### Setup your build environment
1. Download these sources (using git checkout as described in [Using Git])
2. Run the batch file `tools\windows_buildenv.bat`
   - This file downloads the prebuild Mixxx environment, defined in `cmake\windows_build_environment_name` from https://downloads.mixxx.org/builds/buildserver/2.3.x-windows/
   - Generates the `CMakeSettings.json` with the matching build configurations for Visual Studio
3. Start Visual Studio, choose "Open a local folder" select the `mixxx` directory containing `CMakeSettings.json`
4. Menu "Project" -> "Generate Cache for mixxx"
5. Select the build configuration in the toolbar (`x64__portable` is recommended)
6. Menu "Build" -> "Build All"
### Creating an .msi installer (optional)
7. Than open the Visual Studio 'Developer Command Prompt' by Menu -> "Tools" -> "Command line" -> "Developer Command Prompt"
8. Go to your build directory, e.g. by "cd .\build\x64-portable"
9. Run "cpack -G WIX"


Please see also our helpful guide on the [wiki] for more information: [Compiling on Windows]

## Documentation

For help using Mixxx, there are a variety of options:

- [Mixxx manual][manual]
- [Mixxx wiki][wiki]
- [Frequently Asked Questions][FAQ]
- [Hardware Compatibility]
- [Creating Skins]

## Translation

Help to spread Mixxx with translations into more languages, as well as to update and ensure the accuracy of existing translations.

- [Help translate content]
- [Mixxx i18n wiki]
- [Mixxx localization forum]
- [Mixxx glossary]

## Community

Mixxx is a vibrant community of hackers, DJs and artists. To keep track of
development and community news:

- Chat with us on [Zulip][zulip].
- Follow us on [Twitter] and [Facebook].
- Subscribe to the [Mixxx Blog][blog].
- Post on the [Mixxx forums][discourse].

## License

Mixxx is released under the GPLv2. See the LICENSE file for a full copy of the
license.

[mixxx]: https://mixxx.org
[download-stable]: https://mixxx.org/download/#stable
[download-testing]: https://mixxx.org/download/#testing
[fileabug]: https://bugs.launchpad.net/mixxx/+filebug
[twitter]: https://twitter.com/mixxxdj
[facebook]: https://www.facebook.com/pages/Mixxx-DJ-Software/21723485212
[blog]: https://mixxx.org/news/
[manual]: https://manual.mixxx.org/
[wiki]: https://github.com/mixxxdj/mixxx/wiki
[faq]: https://github.com/mixxxdj/mixxx/wiki/Faq
[Compiling on Linux]: https://github.com/mixxxdj/mixxx/wiki/Compiling%20on%20Linux
[Compiling on MacOS]: https://github.com/mixxxdj/mixxx/wiki/Compiling%20on%20macOS
[Compiling on Windows]: https://github.com/mixxxdj/mixxx/wiki/compiling-on-windows
[Using Git]: https://github.com/mixxxdj/mixxx/wiki/Using-Git
[CMake]: https://cmake.org/
[easybugs]: https://bugs.launchpad.net/mixxx/+bugs?field.searchtext=&orderby=-importance&search=Search&field.status%3Alist=NEW&field.status%3Alist=CONFIRMED&field.status%3Alist=TRIAGED&field.status%3Alist=INPROGRESS&field.status%3Alist=INCOMPLETE_WITH_RESPONSE&field.status%3Alist=INCOMPLETE_WITHOUT_RESPONSE&assignee_option=any&field.assignee=&field.bug_reporter=&field.bug_commenter=&field.subscriber=&field.structural_subscriber=&field.tag=easy&field.tags_combinator=ANY&field.has_cve.used=&field.omit_dupes.used=&field.omit_dupes=on&field.affects_me.used=&field.has_patch.used=&field.has_branches.used=&field.has_branches=on&field.has_no_branches.used=&field.has_no_branches=on&field.has_blueprints.used=&field.has_blueprints=on&field.has_no_blueprints.used=&field.has_no_blueprints=on
[creating skins]: https://mixxx.org/wiki/doku.php/Creating-Skins
[help translate content]: https://www.transifex.com/projects/p/mixxxdj
[Mixxx i18n wiki]: https://github.com/mixxxdj/mixxx/wiki/Internationalization
[Mixxx localization forum]: https://mixxx.discourse.group/c/translation/13
[Mixxx glossary]: https://www.transifex.com/projects/p/mixxxdj/glossary/l/en/
[hardware compatibility]: https://github.com/mixxxdj/mixxx/wiki/Hardware-Compatibility
[zulip]: https://mixxx.zulipchat.com/
[discourse]: https://mixxx.discourse.group/
