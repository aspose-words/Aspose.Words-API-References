---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /tr/python-net/aspose.words/document/font_settings/
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
# Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# İkinci yazı tipi, "Amethysta", mevcut değil.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Yazı tipi ikame tablosunu yapılandırabiliriz ve bu tablo belirler
# hangi yazı tiplerinin Aspose.Words tarafından mevcut olmayan yazı tipleri için ikame olarak kullanılacağını.
# "Amethysta" için iki ikame yazı tipini ayarlayın: "Arvo" ve "Courier New".
# İlk ikame mevcut değilse, Aspose.Words ikinci ikameyi kullanmayı dener ve bu şekilde devam eder.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" mevcut değil ve ikame kuralı, ikame olarak kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" da mevcut değil, ancak "Courier New" mevcut.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Çıktı belgesi, "Amethysta" yazı tipini kullanan metni "Courier New" ile biçimlendirilmiş olarak gösterecek.
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

