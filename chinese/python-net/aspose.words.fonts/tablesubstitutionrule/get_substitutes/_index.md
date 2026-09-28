---
title: TableSubstitutionRule.get_substitutes method
linktitle: get_substitutes method
articleTitle: get_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.get_substitutes method. Returns array containing substitute font names for the specified original font name."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fonts/tablesubstitutionrule/get_substitutes/
---

## get_substitutes(original_font_name) {#str}

Returns array containing substitute font names for the specified original font name.


```python
def get_substitutes(self, original_font_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| original_font_name | str | Original font name. |

### Returns

List of alternative font names.


### Examples

Shows how to access a document's system font source and set font substitutes.

```python
import platform
from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR

class TestFontSubstitution(ApiExampleBase):

    def test_font_substitution(self):
        doc = aw.Document()
        doc.font_settings = aw.fonts.FontSettings()
        # 默认情况下，空白文档始终包含系统字体源。
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        system_font_source = doc.font_settings.get_fonts_sources()[0].as_system_font_source()
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, system_font_source.type)
        self.assertEqual(0, system_font_source.priority)
        is_windows = platform.system() == 'Windows'
        if is_windows:
            fonts_path = 'C:\\WINDOWS\\Fonts'
            actual = None
            cond_expression = next(iter(aw.fonts.SystemFontSource.get_system_font_folders()), None)
            if cond_expression is not None:
                actual = cond_expression.lower()
            self.assertEqual(fonts_path.lower(), actual)
        for system_font_folder in aw.fonts.SystemFontSource.get_system_font_folders():
            print(system_font_folder)
        # 将 Windows 字体目录中存在的字体设置为不存在的字体的替代品。
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # 或者，我们可以添加一个文件夹字体源，其中相应的文件夹包含该字体。
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # 重置字体源后，仍然保留系统字体源以及我们的替代字体。
        doc.font_settings.reset_font_sources()
        self.assertEqual(1, len(doc.font_settings.get_fonts_sources()))
        self.assertEqual(aw.fonts.FontSourceType.SYSTEM_FONTS, doc.font_settings.get_fonts_sources()[0].type)
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertTrue(doc.font_settings.substitution_settings.font_name_substitution.enabled)
```

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
* class [TableSubstitutionRule](../)

