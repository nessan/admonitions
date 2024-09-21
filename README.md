# Quarto Extension `admonitions`

The `admonitions` filter adds simple AsciiDoc-style paragraph [admonitions][] to [Quarto][].

TIP: Set the DEBUG flag at compile time to enable range-checking on indices. \
       However, remember that range-checking can slow your code down by orders of magnitude.

Using

Use the extension to draw attention to a paragraph. Start the first line of the paragraph with one of the following  five labels:

- NOTE:
- WARNING:
- TIP:
- CAUTION:
- IMPORTANT:

The label must be in uppercase and followed by a colon ( : ).

For example:

```markdown
TIP: Set the DEBUG flag at compile time to enable range-checking on indices. \
     However, remember that range-checking can slow your code down by orders of magnitude.
```

This will be rendered as:

![README-tip](assets/README-tip.png)

Each admonition type has its particular icon, and the admonition content on the right can contain arbitrary markdown.

## Admonitions vs. Callouts

Quarto already has [callout blocks][], which are a very similar concept, though with a wordier syntax.

For example:

```markdown
::: {.callout-tip}
TIP: Set the DEBUG flag at compile time to enable range-checking on indices. \
     However, remember that range-checking can slow your code down by orders of magnitude.
:::
```

This will be rendered as:

![README-callout](assets/README-callout.png)

The markup for an admonition is simple and clean without resorting to a custom `div`.

Of course, you can mix and match both styles without a problem.

## Installing

The command

```bash
quarto add nessan/admonitions
```

installs the extension under the `extensions` subdirectory, which should be checked in if you use version control.
Once it is installed, you add the extension as a filter in your `_quarto.yml` file as usual:

```yml
filters:
    - admonitions
```

## Examples

See the `examples` directory for demonstration projects using this extension.

## Acknowledgements

This extension is inspired by the simplicity of [AsciiDoc][] admonitions and uses similar `CSS` to style the output.

AsciiDoc also has the concept of a *block* admonition, which is not replicated in this extension, as Quarto's callout blocks work perfectly well for that purpose.

## TODO

1. Customising the filter should be possible, such as letting the user change the icons associated with the various admonitions.
2. The filter only handles `HTML` output.

## Contact

You can contact me by email [here](mailto:nzznfitz+gh@icloud.com).

## Copyright and License

Copyright (c) 2024-present Nessan Fitzmaurice.
You can use this software under the [MIT license][].

<!-- Reference links -->

[Quarto]: https://quarto.org
[AsciiDoc]: https://docs.asciidoctor.org/asciidoc/latest/
[admonitions]: https://docs.asciidoctor.org/asciidoc/latest/blocks/admonitions/
[callout blocks]: https://quarto.org/docs/authoring/callouts.html
[MIT license]: https://opensource.org/license/mit
