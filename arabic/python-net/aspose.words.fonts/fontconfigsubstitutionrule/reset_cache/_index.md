---
title: FontConfigSubstitutionRule.reset_cache method
linktitle: reset_cache method
articleTitle: reset_cache method
second_title: Aspose.Words for Python
description: "FontConfigSubstitutionRule.reset_cache method. Resets the cache of fontconfig calling results."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fonts/fontconfigsubstitutionrule/reset_cache/
---

## reset_cache() {#default}

Resets the cache of fontconfig calling results.


```python
def reset_cache(self):
    ...
```

### Examples

Shows operating system-dependent font config substitution.

```python
font_settings = aw.fonts.FontSettings()
font_config_substitution = font_settings.substitution_settings.font_config_substitution
# كائن FontConfigSubstitutionRule يعمل بشكل مختلف على منصات Windows/غير Windows.
# على Windows، هو غير متوفر.
# على Linux/Mac، سيكون لدينا إمكانية الوصول إليه، وسنتمكن من تنفيذ العمليات.
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

