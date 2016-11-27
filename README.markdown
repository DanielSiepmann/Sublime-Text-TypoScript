Based on the work by Enrique Moreno Tent on [Github](https://github.com/search?q=typoscript&ref=opensearch).

## Features
- Some additional _keywords_ like ``FLUIDTEMPLATE``.
- Added the ability to comment and uncomment via Sublime Text functionality (menu and keyboard).
- Highlighting for TypoScript conditions
- Highlighting for deprecated _keywords_ (TYPO3 7.x)

## Supported files

The package will apply the syntax automatically to files to ``*.ts``, ``*.ts2``, ``*.t3``, ``*.t3c``, ``*.t3s`` files.

By installing the [ApplySyntax][] package some of TYPO3s ``*.txt`` files are covered as well:

* ``ext_conf_template.txt``
* ``ext_typoscript_constants.txt``
* ``ext_typoscript_setup.txt``
* ``constants.txt`` (*)
* ``setup.txt`` (*)

\*) As long as their paths contain the strings ``fileadmin``, ``typo3`` or ``TypoScript``.

The ``ApplySyntax`` configuration actually looks like this:

    {
        "syntaxes": [
            {
                "syntax": "TypoScript/TypoScript",
                "rules": [
                    {"file_path": ".*(\\\\|/)ext_conf_template\\.txt$"},
                    {"file_path": ".*(\\\\|/)ext_typoscript_(setup|constants)\\.txt$"},
                    {"file_name": ".*(\\\\|/)(fileadmin|typo3|TypoScript).*(\\\\|/)(setup|constants)\\.txt$"}
                ]
            }
        ]
    }

To apply TypoScript syntax highlighting to other files you could easily enhance the above syntax detection rules. Have a look into the [ApplySyntax manual][]

Thanks to [Philipp Kitzberger][] and [Mathias Brodala][] for the hint.

[ApplySyntax]: https://github.com/facelessuser/ApplySyntax
[ApplySyntax manual]: http://facelessuser.github.io/ApplySyntax/usage/#overview
[Philipp Kitzberger]: https://github.com/Kitzberger
[Mathias Brodala]: https://github.com/mbrodala
