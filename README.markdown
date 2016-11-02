Based on the work by Enrique Moreno Tent on [Github](https://github.com/search?q=typoscript&ref=opensearch).

## Features
- Some additional _keywords_ like ``FLUIDTEMPLATE``.
- Added the ability to comment and uncomment via Sublime Text functionality (menu and keyboard).

## Supported files

The package will apply the syntax to ``*.ts`` files.  
You can create your own rules using the [ApplySyntax][] package with this configuration:

    {
        "syntaxes": [
            {
                "name": "TypoScript/TypoScript",
                "rules": [
                    {"file_name": ".*\\\\ext_conf_template\\.txt$"},
                    {"file_name": ".*\\\\ext_typoscript_(setup|constants)\\.txt$"},
                    {"file_name": ".*\\\\(setup|constants)\\.txt$"}
                ]
            }
        ]
    }

Thanks at [Philipp Kitzberger][] for the hint.

[ApplySyntax]: https://github.com/facelessuser/ApplySyntax
[Philipp Kitzberger]: https://bitbucket.org/kitze
