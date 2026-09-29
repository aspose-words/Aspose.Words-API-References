---
title: FontSubstitutionRule class
linktitle: FontSubstitutionRule class
articleTitle: FontSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSubstitutionRule class. This is an abstract base class for the font substitution rule"
type: docs
weight: 190
url: /sv/python-net/aspose.words.fonts/fontsubstitutionrule/
---

## FontSubstitutionRule class

This is an abstract base class for the font substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [enabled](./enabled/) | Specifies whether the rule is enabled or not. |

### Examples

Shows operating system-dependent font config substitution.

```python
font_settings = aw.fonts.FontSettings()
font_config_substitution = font_settings.substitution_settings.font_config_substitution
# FontConfigSubstitutionRule-objektet fungerar annorlunda på Windows-/icke‑Windows‑plattformar.
# På Windows är det inte tillgängligt.
# På Linux/Mac kommer vi att ha åtkomst till det och kunna utföra operationer.
is_windows = os.name == 'nt'
is_linux_or_mac = not is_windows
if is_windows:
    assert not font_config_substitution.enabled
    assert not font_config_substitution.is_font_config_available()
if is_linux_or_mac:
    assert font_config_substitution.enabled
    assert font_config_substitution.is_font_config_available()
font_config_substitution.reset_cache()
```

### See Also

* module [aspose.words.fonts](../)

