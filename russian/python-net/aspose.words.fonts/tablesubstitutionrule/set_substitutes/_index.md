---
title: TableSubstitutionRule.set_substitutes method
linktitle: set_substitutes method
articleTitle: set_substitutes method
second_title: Aspose.Words for Python
description: "TableSubstitutionRule.set_substitutes method. Override substitute font names for given original font name."
type: docs
weight: 80
url: /ru/python-net/aspose.words.fonts/tablesubstitutionrule/set_substitutes/
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

Shows how set font substitution rules.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Arial'
builder.writeln('Hello world!')
builder.font.name = 'Amethysta'
builder.writeln('The quick brown fox jumps over the lazy dog.')
font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Источник шрифтов по умолчанию содержит первый шрифт, используемый документом.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# Второй шрифт, "Amethysta", недоступен.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Мы можем настроить таблицу замены шрифтов, которая определяет
# какие шрифты Aspose.Words будет использовать в качестве замен для недоступных шрифтов.
# Установите два заменяющих шрифта для "Amethysta": "Arvo" и "Courier New".
# Если первая замена недоступна, Aspose.Words пытается использовать вторую замену и так далее.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" недоступен, и правило замены указывает, что первым шрифтом для замены является "Arvo".
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" также недоступен, но "Courier New" доступен.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Выходной документ отобразит текст, использующий шрифт "Amethysta", отформатированный шрифтом "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
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

