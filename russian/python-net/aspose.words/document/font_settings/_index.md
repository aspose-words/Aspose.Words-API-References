---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /ru/python-net/aspose.words/document/font_settings/
---

## Document.font_settings property

Gets or sets document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

This property allows to specify font settings per document. If set to ``None``, default static font settings
[FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




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

### See Also

* module [aspose.words](../../)
* class [Document](../)

