---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /ru/python-net/aspose.words.fonts/fontsettings/default_instance/
---

## FontSettings.default_instance property

Static default font settings.


```python
@property
def default_instance(self) -> aspose.words.fonts.FontSettings:
    ...

```

### Remarks

This instance is used by default in a document unless [Document.font_settings](../../../aspose.words/document/font_settings/) is specified.



### Examples

Shows how to configure the default font settings instance.

```python
# Настройте экземпляр настроек шрифтов по умолчанию использовать шрифт "Courier New"
# в качестве резервной замены, когда мы пытаемся использовать неизвестный шрифт.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
# У этого документа нет конфигурации FontSettings. При рендеринге документа,
# экземпляр FontSettings по умолчанию разрешит отсутствующий шрифт.
# Aspose.Words будет использовать "Courier New" для рендеринга текста, использующего неизвестный шрифт.
self.assertIsNone(doc.font_settings)
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.DefaultFontInstance.pdf')
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Times New Roman'
builder.writeln('Hello world!')
callback = self.FontSubstitutionWarningCollector()
doc.warning_callback = callback
# Сохраните текущую коллекцию источников шрифтов, которая будет использоваться как источник шрифтов по умолчанию для каждого документа
# для которых мы не указываем иной источник шрифтов.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Для целей тестирования мы установим Aspose.Words искать шрифты только в папке, которой не существует.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# При рендеринге документа не будет места, где можно найти шрифт "Times New Roman".
# Это вызовет предупреждение о замене шрифта, которое наш обратный вызов обнаружит.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.SubstitutionWarning.pdf')
aw.fonts.FontSettings.default_instance.set_fonts_sources(sources=original_font_sources)
self.assertEqual(1, callback.font_substitution_warnings.count)
self.assertTrue(callback.font_substitution_warnings[0].warning_type == aw.WarningType.FONT_SUBSTITUTION)
self.assertTrue(callback.font_substitution_warnings[0].description == "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.")
```

Shows how to use the IWarningCallback interface to monitor font substitution warnings (FontSubstitutionWarningCollector).

```python
class FontSubstitutionWarningCollector(aw.IWarningCallback):

    def __init__(self):
        self.font_substitution_warnings = aw.WarningInfoCollection()

    def warning(self, info):
        if info.warning_type == aw.WarningType.FONT_SUBSTITUTION:
            self.font_substitution_warnings.warning(info)
```

### See Also

* module [aspose.words.fonts](../../)
* class [FontSettings](../)

