---
title: FontConfigSubstitutionRule.is_font_config_available method
linktitle: is_font_config_available method
articleTitle: is_font_config_available method
second_title: Aspose.Words for Python
description: "FontConfigSubstitutionRule.is_font_config_available method. Check if fontconfig utility is available or not."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fonts/fontconfigsubstitutionrule/is_font_config_available/
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

* module [aspose.words.fonts](../../)
* class [FontConfigSubstitutionRule](../)

