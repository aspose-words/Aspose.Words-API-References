---
title: LoadOptions.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "LoadOptions.font_settings property. Allows to specify document font settings."
type: docs
weight: 60
url: /ru/python-net/aspose.words.loading/loadoptions/font_settings/
---

## LoadOptions.font_settings property

Allows to specify document font settings.


```python
@property
def font_settings(self) -> aspose.words.fonts.FontSettings:
    ...

@font_settings.setter
def font_settings(self, value: aspose.words.fonts.FontSettings):
    ...

```

### Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words
may resolve the fonts to perform font fallback.

If set to ``None``, default static font settings [FontSettings.default_instance](../../../aspose.words.fonts/fontsettings/default_instance/) will be used.

The default value is ``None``.




### Examples

Shows how to designate font substitutes during loading.

```python
load_options = aw.loading.LoadOptions()
load_options.font_settings = aw.fonts.FontSettings()
# Установите правило замены шрифтов для объекта LoadOptions.
# Если документ, который мы загружаем, использует шрифт, которого у нас нет,
# это правило заменит недоступный шрифт на существующий.
# В этом случае все вхождения "MissingFont" будут преобразованы в "Comic Sans MS".
substitution_rule = load_options.font_settings.substitution_settings.table_substitution
substitution_rule.add_substitutes('MissingFont', ['Comic Sans MS'])
doc = aw.Document(file_name=MY_DIR + 'Missing font.html', load_options=load_options)
# На данном этапе такой текст всё ещё будет в "MissingFont".
# Замена шрифтов произойдёт при рендеринге документа.
self.assertEqual('MissingFont', doc.first_section.body.first_paragraph.runs[0].font.name)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.ResolveFontsBeforeLoadingDocument.pdf')
```

Shows how to apply font substitution settings while loading a document.

```python
# Создайте объект FontSettings, который заменит шрифт "Times New Roman"
# на шрифт "Arvo" из нашей папки "MyFonts".
font_settings = aw.fonts.FontSettings()
font_settings.set_fonts_folder(FONTS_DIR, False)
font_settings.substitution_settings.table_substitution.add_substitutes('Times New Roman', ['Arvo'])
# Установите этот объект FontSettings в качестве свойства вновь созданного объекта LoadOptions.
load_options = aw.loading.LoadOptions()
load_options.font_settings = font_settings
# Загрузите документ, затем отрендерите его в PDF с заменой шрифтов.
doc = aw.Document(file_name=MY_DIR + 'Document.docx', load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'LoadOptions.FontSettings.pdf')
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

