---
title: TableSubstitutionRule.load_linux_settings method
linktitle: load_linux_settings method
articleTitle: load_linux_settings method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.load_linux_settings method. Loads predefined table substitution settings for Linux platform."
type: docs
weight: 50
url: /python-net/aspose.words.fonts/tablesubstitutionrule/load_linux_settings/
---

## load_linux_settings() {#default}

Loads predefined table substitution settings for Linux platform.


```python
def load_linux_settings(self):
    ...
```

### Examples

Shows how to access font substitution tables for Windows and Linux.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
table_substitution_rule = font_settings.substitution_settings.table_substitution
table_substitution_rule.load_windows_settings()
self.assertEqual(['Times New Roman'], table_substitution_rule.get_substitutes('Times New Roman CE'))
table_substitution_rule.save(ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Windows.xml')
table_substitution_rule.load_linux_settings()
self.assertEqual(['FreeSerif', 'Liberation Serif', 'DejaVu Serif'], table_substitution_rule.get_substitutes('Times New Roman CE'))
with system_helper.io.FileStream(ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Linux.xml', system_helper.io.FileMode.CREATE) as file_stream:
    table_substitution_rule.save(output_stream=file_stream)
# Verify Windows XML
xml_content = system_helper.io.File.ReadAllText(ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Windows.xml')
fallback_settings_doc = ET.fromstring(xml_content)
rules = fallback_settings_doc.findall('.//{Aspose.Words}Item')
self.assertEqual('Times New Roman CE', rules[16].get('OriginalFont'))
self.assertEqual('Times New Roman', rules[16].get('SubstituteFonts'))
# Verify Linux XML
xml_content = system_helper.io.File.ReadAllText(ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Linux.xml')
fallback_settings_doc = ET.fromstring(xml_content)
rules = fallback_settings_doc.findall('.//{Aspose.Words}Item')
self.assertEqual('Times New Roman CE', rules[31].get('OriginalFont'))
self.assertEqual('FreeSerif, Liberation Serif, DejaVu Serif', rules[31].get('SubstituteFonts'))
```

### See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

