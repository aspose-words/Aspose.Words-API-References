---
title: FontConfigSubstitutionRule class
second_title: Aspose.Words for Python via .NET API Reference
description: "Font config substitution rule"
type: docs
weight: 60
url: /python-net/aspose.words.fonts/fontconfigsubstitutionrule/
---

## FontConfigSubstitutionRule class

Font config substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




This rule uses fontconfig utility on Linux (and other Unix-like) platforms to get the substitution
if the original font is not available.

If fontconfig utility is not available then this rule will be ignored.




**Inheritance:** [FontConfigSubstitutionRule](./) → [FontSubstitutionRule](../fontsubstitutionrule/)

### Properties

| Name | Description |
| --- | --- |
| [enabled](./enabled/) | Specifies whether the rule is enabled or not. |

### Methods

| Name | Description |
| --- | --- |
|[ is_font_config_available()](./is_font_config_available/#default) | Check if fontconfig utility is available or not. |
|[ reset_cache()](./reset_cache/#default) | Resets the cache of fontconfig calling results. |

### Examples

Shows operating system-dependent font config substitution.

```python
font_settings = aw.fonts.FontSettings()
font_config_substitution = font_settings.substitution_settings.font_config_substitution

# The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
# On Windows, it is unavailable.
if platform.system() == "Windows":
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
* class [FontSubstitutionRule](../fontsubstitutionrule/)

