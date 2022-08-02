---
title: add_substitutes method
second_title: Aspose.Words for Python via .NET API Reference
description: "Adds substitute font names for given original font name."
type: docs
weight: 10
url: /python-net/aspose.words.fonts/tablesubstitutionrule/add_substitutes/
---

## add_substitutes(original_font_name, substitute_font_names) {#str_strlist}

Adds substitute font names for given original font name.


```python
def add_substitutes(self, original_font_name: str, substitute_font_names: List[str]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str |  |
| substitute_font_names | List[str] |  |

### Examples

Shows how to access a document's system font source and set font substitutes.

```python
doc = aw.Document()
doc.font_settings = aw.fonts.FontSettings()

# By default, a blank document always contains a system font source.
self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))

system_font_source = doc.font_settings.get_fonts_sources()[0]
self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
self.assertEqual(0, system_font_source.priority)

if platform.system() == "Windows":
    fonts_path = "C:\\WINDOWS\\Fonts"
    self.assertEqual(fonts_path.lower(), aw.fonts.SystemFontSource.get_system_font_folders()[0].lower())

for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():

    print(system_font_folder)

# Set a font that exists in the Windows Fonts directory as a substitute for one that does not.
doc.font_settings.substitution_settings.font_info_substitution.enabled = True
doc.font_settings.substitution_settings.table_substitution.add_substitutes("Kreon-Regular", ["Calibri"])

self.assertEqual(1, len(list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular"))))
self.assertIn("Calibri", list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular")))

# Alternatively, we could add a folder font source in which the corresponding folder contains the font.
folder_font_source = aw.fonts.FolderFontSource(FONTS_DIR, False)
doc.font_settings.set_fonts_sources([system_font_source, folder_font_source])
self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))

# Resetting the font sources still leaves us with the system font source as well as our substitutes.
doc.font_settings.reset_font_sources()

self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
self.assertEqual(1, len(list(doc.font_settings.substitution_settings.table_substitution.get_substitutes("Kreon-Regular"))))
```

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

### See Also

* module [aspose.words.fonts](../../)
* class [TableSubstitutionRule](../)

