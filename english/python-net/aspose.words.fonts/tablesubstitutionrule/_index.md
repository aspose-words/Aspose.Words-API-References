---
title: TableSubstitutionRule class
linktitle: TableSubstitutionRule class
articleTitle: TableSubstitutionRule class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.TableSubstitutionRule class. Table font substitution rule"
type: docs
weight: 250
url: /python-net/aspose.words.fonts/tablesubstitutionrule/
---

## TableSubstitutionRule class

Table font substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




### Remarks

This rule defines the list of substitute font names to be used if the original font is not available.
Substitutes will be checked for the font name and the [FontInfo.alt_name](../fontinfo/alt_name/) (if any).



**Inheritance:** [TableSubstitutionRule](./) → [FontSubstitutionRule](../fontsubstitutionrule/)

### Properties

| Name | Description |
| --- | --- |
| [enabled](../fontsubstitutionrule/enabled/) | Specifies whether the rule is enabled or not.<br>(Inherited from [FontSubstitutionRule](../fontsubstitutionrule/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add_substitutes(original_font_name, substitute_font_names)](./add_substitutes/#str_strlist) | Adds substitute font names for given original font name. |
|[ get_substitutes(original_font_name)](./get_substitutes/#str) | Returns array containing substitute font names for the specified original font name. |
|[ load(file_name)](./load/#str) | Loads table substitution settings from XML file. |
|[ load(stream)](./load/#bytesio) | Loads table substitution settings from XML stream. |
|[ load_android_settings()](./load_android_settings/#default) | Loads predefined table substitution settings for Android platform. |
|[ load_linux_settings()](./load_linux_settings/#default) | Loads predefined table substitution settings for Linux platform. |
|[ load_windows_settings()](./load_windows_settings/#default) | Loads predefined table substitution settings for Windows platform. |
|[ save(file_name)](./save/#str) | Saves the current table substitution settings to file. |
|[ save(output_stream)](./save/#bytesio) | Saves the current table substitution settings to stream. |
|[ set_substitutes(original_font_name, substitute_font_names)](./set_substitutes/#str_strlist) | Override substitute font names for given original font name. |

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

* module [aspose.words.fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

