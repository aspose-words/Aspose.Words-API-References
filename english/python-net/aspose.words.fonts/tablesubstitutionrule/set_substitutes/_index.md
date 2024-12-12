---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
---

## set_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Override substitute font names for given original font name.


```python
def set_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |
| substitute_font_names | List[str] | List of alternative font names. |

### Examples

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
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Below are two ways of loading a substitution table from a file in the local file system.
# 1 -  From a stream:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Directly from a file:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Since we no longer have access to "Arial", our font table will first try substitute it with "Nonexistent Font".
# We do not have this font so that it will move onto the next substitute, "Kreon", found in the "MyFonts" folder.
self.assertSequenceEqual(['Missing Font', 'Kreon'], list(table_substitution_rule.get_substitutes('Arial')))
# We can expand this table programmatically. We will add an entry that substitutes "Times New Roman" with "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertSequenceEqual(['Arvo'], list(table_substitution_rule.get_substitutes('Times New Roman')))
# We can add a secondary fallback substitute for an existing font entry with AddSubstitutes().
# In case "Arvo" is unavailable, our table will look for "M+ 2m" as a second substitute option.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertSequenceEqual(['Arvo', 'M+ 2m'], list(table_substitution_rule.get_substitutes('Times New Roman')))
# SetSubstitutes() can set a new list of substitute fonts for a font.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertSequenceEqual(['Squarish Sans CT', 'M+ 2m'], list(table_substitution_rule.get_substitutes('Times New Roman')))
# Writing text in fonts that we do not have access to will invoke our substitution rules.
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Text written in Arial, to be substituted by Kreon.')
builder.font.name = 'Times New Roman'
builder.writeln('Text written in Times New Roman, to be substituted by Squarish Sans CT.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Custom.pdf')
```

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# The default font sources contain the first font that the document uses.
self.assertEqual(1, len(font_sources))
self.assertTrue(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Arial')))
# The second font, "Amethysta", is unavailable.
self.assertFalse(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Amethysta')))
# We can configure a font substitution table which determines
# which fonts Aspose.Words will use as substitutes for unavailable fonts.
# Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
# If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
self.assertFalse(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Arvo')))
# "Arvo" is also unavailable, but "Courier New" is.
self.assertTrue(any((f for f in font_sources[0].get_available_fonts() if f.full_font_name == 'Courier New')))
# The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
doc.save(ARTIFACTS_DIR + 'FontSettings.table_substitution.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

