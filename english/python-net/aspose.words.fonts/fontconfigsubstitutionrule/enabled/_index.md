---
title: FontConfigSubstitutionRule.enabled property
linktitle: enabled property
articleTitle: enabled property
second_title: Aspose.Words for Python
description: "FontConfigSubstitutionRule.enabled property. Specifies whether the rule is enabled or not."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/fontconfigsubstitutionrule/enabled/
---

## FontConfigSubstitutionRule.enabled property

Specifies whether the rule is enabled or not.


```python
@property
def enabled(self) -> bool:
    ...

@enabled.setter
def enabled(self, value: bool):
    ...

```

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

* module [aspose.words.fonts](../../)
* class [FontConfigSubstitutionRule](../)

