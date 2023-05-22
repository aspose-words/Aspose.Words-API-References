---
title: FontConfigSubstitutionRule.is_font_config_available method
linktitle: is_font_config_available method
articleTitle: is_font_config_available method
second_title: Aspose.Words for Python
description: "FontConfigSubstitutionRule.is_font_config_available method. Check if fontconfig utility is available or not."
type: docs
weight: 20
url: /python-net/aspose.words.fonts/fontconfigsubstitutionrule/is_font_config_available/
---

## is_font_config_available() {#default}

Check if fontconfig utility is available or not.


```python
def is_font_config_available(self):
    ...
```

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

* module [aspose.words.fonts](../../)
* class [FontConfigSubstitutionRule](../)

