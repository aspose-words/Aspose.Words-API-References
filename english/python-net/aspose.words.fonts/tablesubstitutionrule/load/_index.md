---
title: TableSubstitutionRule.load method
linktitle: load method
articleTitle: load method
second_title: Aspose.Words for Python
description: "aspose.words.fonts.TableSubstitutionRule.load method"
type: docs
weight: 30
url: /python-net/aspose.words.fonts/tablesubstitutionrule/load/
---

## load(file_name) {#str}

Loads table substitution settings from XML file.


```python
def load(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |

## load(stream) {#bytesio}

Loads table substitution settings from XML stream.


```python
def load(self, stream: BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | BytesIO |  |

## Examples

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings

# Create a new table substitution rule and load the default Windows font substitution table.
table_substitution_rule = font_settings.substitution_settings.table_substitution

# If we select fonts exclusively from our folder, we will need a custom substitution table.
# We will no longer have access to the Microsoft Windows fonts,
# such as "Arial" or "Times New Roman" since they do not exist in our new font folder.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, False)
font_settings.set_fonts_sources([folder_font_source])

# Below are two ways of loading a substitution table from a file in the local file system.
# 1 -  From a stream:
with open(MY_DIR + "Font substitution rules.xml", "rb") as file_stream:
    table_substitution_rule.load(file_stream)

# 2 -  Directly from a file:
table_substitution_rule.load(MY_DIR + "Font substitution rules.xml")

# Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
# We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
self.assertListEqual(["Missing Font", "Kreon"], list(table_substitution_rule.get_substitutes("Arial")))

# We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes("Times New Roman"))
table_substitution_rule.add_substitutes("Times New Roman", ["Arvo"])
self.assertListEqual(["Arvo"], list(table_substitution_rule.get_substitutes("Times New Roman")))

# We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
# In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
table_substitution_rule.add_substitutes("Times New Roman", ["M+ 2m"])
self.assertListEqual(["Arvo", "M+ 2m"], list(table_substitution_rule.get_substitutes("Times New Roman")))

# set_substitutes() can set a new list of substitute fonts for a font.
table_substitution_rule.set_substitutes("Times New Roman", ["Squarish Sans CT", "M+ 2m"])
self.assertListEqual(["Squarish Sans CT", "M+ 2m"], list(table_substitution_rule.get_substitutes("Times New Roman")))

# Writing text in fonts that we do not have access to will invoke our substitution rules.
builder = aw.DocumentBuilder(doc)
builder.font.name = "Arial"
builder.writeln("Text written in Arial, to be substituted by Kreon.")

builder.font.name = "Times New Roman"
builder.writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.")

doc.save(ARTIFACTS_DIR + "FontSettings.table_substitution_rule_custom.pdf")
```

## See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

