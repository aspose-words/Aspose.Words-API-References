---
title: FontConfigSubstitutionRule.enabled property
linktitle: enabled property
articleTitle: enabled property
second_title: Aspose.Words for Python
description: "FontConfigSubstitutionRule.enabled property. Specifies whether the rule is enabled or not."
type: docs
weight: 10
url: /it/python-net/aspose.words.fonts/fontconfigsubstitutionrule/enabled/
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
# L'oggetto FontConfigSubstitutionRule funziona in modo diverso su piattaforme Windows/non-Windows.
# Su Windows, non è disponibile.
# Su Linux/Mac, avremo accesso ad esso e potremo eseguire operazioni.
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

