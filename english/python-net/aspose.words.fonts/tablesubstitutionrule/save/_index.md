---
title: TableSubstitutionRule.save method
linktitle: save method
articleTitle: save method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.TableSubstitutionRule.save method"
type: docs
weight: 70
url: /python-net/aspose.words.fonts/tablesubstitutionrule/save/
---

## save(file_name) {#str}

Saves the current table substitution settings to file.


```python
def save(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | Output file name. |

## save(output_stream) {#bytesio}

Saves the current table substitution settings to stream.


```python
def save(self, output_stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| output_stream | io.BytesIO | Output stream. |

## Examples

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

## See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

