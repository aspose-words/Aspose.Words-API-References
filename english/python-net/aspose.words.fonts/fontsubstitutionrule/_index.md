---
title: FontSubstitutionRule class
linktitle: FontSubstitutionRule class
articleTitle: FontSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontSubstitutionRule class. This is an abstract base class for the font substitution rule"
type: docs
weight: 190
url: /python-net/aspose.words.fonts/fontsubstitutionrule/
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
# The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
# On Windows, it is unavailable.
if platform.system() == 'Windows':
    self.assertFalse(font_config_substitution.enabled)
    self.assertFalse(font_config_substitution.is_font_config_available())
else:
    # On Linux/Mac, we will have access to it, and will be able to perform operations.
    self.assertTrue(font_config_substitution.enabled)
    self.assertTrue(font_config_substitution.is_font_config_available())
    font_config_substitution.reset_cache()
```

### See Also

* module [aspose.words.fonts](../)

