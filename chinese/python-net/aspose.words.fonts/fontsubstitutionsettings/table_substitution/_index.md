---
title: FontSubstitutionSettings.table_substitution property
linktitle: table_substitution property
articleTitle: table_substitution property
second_title: Aspose.Words for Python
description: "FontSubstitutionSettings.table_substitution property. Settings related to table substitution rule."
type: docs
weight: 50
url: /zh/python-net/aspose.words.fonts/fontsubstitutionsettings/table_substitution/
---

## FontSubstitutionSettings.table_substitution property

Settings related to table substitution rule.


```python
@property
def table_substitution(self) -> aspose.words.fonts.TableSubstitutionRule:
    ...

```

### Examples

Shows how to work with custom font substitution tables.

```python
doc = aw.Document()
font_settings = aw.fonts.FontSettings()
doc.font_settings = font_settings
# 创建新的表替换规则并加载默认的 Windows 字体替换表。
table_substitution_rule = font_settings.substitution_settings.table_substitution
# 如果我们仅从自己的文件夹中选择字体，则需要自定义替换表。
# 我们将不再能够访问 Microsoft Windows 字体，
# 例如 "Arial" 或 "Times New Roman"，因为它们在我们的新字体文件夹中不存在。
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# 以下是从本地文件系统中的文件加载替换表的两种方法。
# 1 - 从流中：
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 - 直接从文件中：
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# 由于我们不再能够访问 "Arial"，我们的字体表将首先尝试用 "Nonexistent Font" 替代它。
# 我们没有此字体，因此它将转而使用在 "MyFonts" 文件夹中找到的下一个替代字体 "Kreon"。
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# 我们可以以编程方式扩展此表。我们将添加一条将 "Times New Roman" 替换为 "Arvo" 的条目。
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# 我们可以使用 AddSubstitutes() 为现有字体条目添加次要回退替代。
# 如果 "Arvo" 不可用，我们的表将查找 "M+ 2m" 作为第二替代选项。
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() 可以为字体设置新的替代字体列表。
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# 使用我们无法访问的字体编写文本将触发我们的替代规则。
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Text written in Arial, to be substituted by Kreon.')
builder.font.name = 'Times New Roman'
builder.writeln('Text written in Times New Roman, to be substituted by Squarish Sans CT.')
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitutionRule.Custom.pdf')
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSubstitutionSettings](../)

