---
title: TableSubstitutionRule class
second_title: Aspose.Words for Python via .NET API Reference
description: "Table font substitution rule"
type: docs
weight: 230
url: /python-net/aspose.words.fonts/tablesubstitutionrule/
---

## TableSubstitutionRule class

Table font substitution rule.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.




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
|[ load_android_settings()](./load_android_settings/#default) | Loads predefined table substitution settings for Linux platform. |
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

# Create a new table substitution rule and load the default Microsoft Windows font substitution table.
table_substitution_rule = font_settings.substitution_settings.table_substitution
table_substitution_rule.load_windows_settings()

# In Windows, the default substitute for the "Times New Roman CE" font is "Times New Roman".
self.assertListEqual(["Times New Roman"],
    list(table_substitution_rule.get_substitutes("Times New Roman CE")))

# We can save the table in the form of an XML document.
table_substitution_rule.save(ARTIFACTS_DIR + "FontSettings.table_substitution_rule.windows.xml")

# Linux has its own substitution table.
# There are multiple substitute fonts for "Times New Roman CE".
# If the first substitute, "FreeSerif" is also unavailable,
# this rule will cycle through the others in the array until it finds an available one.
table_substitution_rule.load_linux_settings()
self.assertListEqual(["FreeSerif", "Liberation Serif", "DejaVu Serif"],
    list(table_substitution_rule.get_substitutes("Times New Roman CE")))

# Save the Linux substitution table in the form of an XML document using a stream.
with open(ARTIFACTS_DIR + "FontSettings.table_substitution_rule.linux.xml", "wb") as file_stream:
    table_substitution_rule.save(file_stream)
```

### See Also

* module [aspose.words.fonts](../)
* class [FontSubstitutionRule](../fontsubstitutionrule/)

