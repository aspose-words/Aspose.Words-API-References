---
title: FontSubstitutionSettings.font_config_substitution property
linktitle: font_config_substitution property
articleTitle: font_config_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.font_config_substitution property. Settings related to font config substitution rule."
type: docs
weight: 20
url: /de/python-net/aspose.words.fonts/fontsubstitutionsettings/font_config_substitution/
---

## FontSubstitutionSettings.font_config_substitution property

Settings related to font config substitution rule.


```python
@property
def font_config_substitution(self) -> aspose.words.fonts.FontConfigSubstitutionRule:
    ...

```

### Examples

Shows operating system-dependent font config substitution.

```python
font_settings = aw.fonts.FontSettings()
font_config_substitution = font_settings.substitution_settings.font_config_substitution
# Das Objekt FontConfigSubstitutionRule funktioniert auf Windows‑/Nicht‑Windows‑Plattformen unterschiedlich.
# Unter Windows ist es nicht verfügbar.
# Unter Linux/Mac haben wir Zugriff darauf und können Vorgänge ausführen.
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
* class [FontSubstitutionSettings](../)

