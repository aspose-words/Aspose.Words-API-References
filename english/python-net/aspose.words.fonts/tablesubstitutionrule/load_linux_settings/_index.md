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
# Create a new table substitution rule and load the default Microsoft Windows font substitution table.
table_substitution_rule = font_settings.substitution_settings.table_substitution
table_substitution_rule.load_windows_settings()
# In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
self.assertListEqual(['Times New Roman'], list(table_substitution_rule.get_substitutes('Times New Roman CE')))
# We can save the table in the form of an XML document.
table_substitution_rule.save(ARTIFACTS_DIR + 'FontSettings.table_substitution_rule.windows.xml')
# Linux has its own substitution table.
# There are multiple substitute fonts for "Times New Roman CE".
# If the first substitute, "FreeSerif" is also unavailable,
# this rule will cycle through the others in the array until it finds an available one.
table_substitution_rule.load_linux_settings()
self.assertListEqual(['FreeSerif', 'Liberation Serif', 'DejaVu Serif'], list(table_substitution_rule.get_substitutes('Times New Roman CE')))
# Save the Linux substitution table in the form of an XML document using a stream.
with open(ARTIFACTS_DIR + 'FontSettings.table_substitution_rule.linux.xml', 'wb') as file_stream:
    table_substitution_rule.save(file_stream)
```

### See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

