---
title: TableSubstitutionRule.get_substitutes method
linktitle: get_substitutes method
articleTitle: get_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.get_substitutes method. Returns array containing substitute font names for the specified original font name."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fonts/tablesubstitutionrule/get_substitutes/
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
        # По умолчанию пустой документ всегда содержит системный источник шрифтов.
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
        # Установите шрифт, существующий в каталоге Windows Fonts, в качестве замены для отсутствующего шрифта.
        doc.font_settings.substitution_settings.font_info_substitution.enabled = True
        doc.font_settings.substitution_settings.table_substitution.add_substitutes('Kreon-Regular', ['Calibri'])
        self.assertEqual(1, len(doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular')))
        self.assertIn('Calibri', doc.font_settings.substitution_settings.table_substitution.get_substitutes('Kreon-Regular'))
        # В качестве альтернативы мы могли бы добавить источник шрифтов из папки, в которой соответствующая папка содержит шрифт.
        folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
        doc.font_settings.set_fonts_sources(sources=[system_font_source, folder_font_source])
        self.assertEqual(2, len(doc.font_settings.get_fonts_sources()))
        # Сброс источников шрифтов всё равно оставляет у нас системный источник шрифтов, а также наши замены.
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
# Создайте новое правило подстановки таблицы и загрузите таблицу подстановки шрифтов Windows по умолчанию.
table_substitution_rule = font_settings.substitution_settings.table_substitution
# Если мы будем выбирать шрифты исключительно из нашей папки, нам понадобится пользовательская таблица подстановки.
# Мы больше не будем иметь доступа к шрифтам Microsoft Windows,
# таким как "Arial" или "Times New Roman", поскольку они отсутствуют в нашей новой папке шрифтов.
folder_font_source = aw.fonts.FolderFontSource(folder_path=FONTS_DIR, scan_subfolders=False)
font_settings.set_fonts_sources(sources=[folder_font_source])
# Ниже представлены два способа загрузки таблицы подстановки из файла в локальной файловой системе.
# 1 -  Из потока:
with system_helper.io.FileStream(MY_DIR + 'Font substitution rules.xml', system_helper.io.FileMode.OPEN) as file_stream:
    table_substitution_rule.load(stream=file_stream)
# 2 -  Непосредственно из файла:
table_substitution_rule.load(file_name=MY_DIR + 'Font substitution rules.xml')
# Поскольку мы больше не имеем доступа к "Arial", наша таблица шрифтов сначала попытается заменить его на "Nonexistent Font".
# У нас нет этого шрифта, поэтому будет использована следующая замена — "Kreon", найденный в папке "MyFonts".
self.assertEqual(['Missing Font', 'Kreon'], table_substitution_rule.get_substitutes('Arial'))
# Мы можем расширить эту таблицу программно. Мы добавим запись, заменяющую "Times New Roman" на "Arvo"
self.assertIsNone(table_substitution_rule.get_substitutes('Times New Roman'))
table_substitution_rule.add_substitutes('Times New Roman', ['Arvo'])
self.assertEqual(['Arvo'], table_substitution_rule.get_substitutes('Times New Roman'))
# Мы можем добавить вторичную резервную замену для существующей записи шрифта с помощью AddSubstitutes().
# Если "Arvo" недоступен, наша таблица будет искать "M+ 2m" как второй вариант замены.
table_substitution_rule.add_substitutes('Times New Roman', ['M+ 2m'])
self.assertEqual(['Arvo', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# SetSubstitutes() может задать новый список заменяющих шрифтов для шрифта.
table_substitution_rule.set_substitutes('Times New Roman', ['Squarish Sans CT', 'M+ 2m'])
self.assertEqual(['Squarish Sans CT', 'M+ 2m'], table_substitution_rule.get_substitutes('Times New Roman'))
# Запись текста шрифтами, к которым у нас нет доступа, вызовет наши правила замены.
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

