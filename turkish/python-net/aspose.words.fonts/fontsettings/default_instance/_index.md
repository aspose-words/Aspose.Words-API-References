---
title: FontSettings.default_instance property
linktitle: default_instance property
articleTitle: default_instance property
second_title: Aspose.Words for Python
description: "FontSettings.default_instance property. Static default font settings."
type: docs
weight: 20
url: /tr/python-net/aspose.words.fonts/fontsettings/default_instance/
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
# Varsayılan yazı tipi ayarları örneğini "Courier New" yazı tipini kullanacak şekilde yapılandırın
# bilinmeyen bir yazı tipi kullandığımızda yedek ikame olarak.
aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.default_font_name = 'Courier New'
self.assertTrue(aw.fonts.FontSettings.default_instance.substitution_settings.default_font_substitution.enabled)
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
# Bu belgenin bir FontSettings yapılandırması yok. Belgeyi işlediğimizde,
# varsayılan FontSettings örneği eksik yazı tipini çözecek.
# Aspose.Words, bilinmeyen bir yazı tipini kullanan metni işlemek için "Courier New" kullanacak.
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
# Mevcut yazı tipi kaynakları koleksiyonunu saklayın; bu, her belge için varsayılan yazı tipi kaynağı olacaktır
# farklı bir yazı tipi kaynağı belirtmediğimiz durumlar için.
original_font_sources = aw.fonts.FontSettings.default_instance.get_fonts_sources()
# Test amaçları için, Aspose.Words'ı yalnızca var olmayan bir klasörde yazı tiplerini arayacak şekilde ayarlayacağız.
aw.fonts.FontSettings.default_instance.set_fonts_folder('', False)
# Belge render edildiğinde, "Times New Roman" yazı tipini bulacak bir yer olmayacaktır.
# Bu, bir yazı tipi ikame uyarısına neden olacak ve geri çağrımımız bunu tespit edecek.
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

