---
title: Document.font_settings property
linktitle: font_settings property
articleTitle: font_settings property
second_title: Aspose.Words for Python
description: "Document.font_settings property. Gets or sets document font settings."
type: docs
weight: 150
url: /de/python-net/aspose.words/document/font_settings/
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
# Die standardmäßigen Schriftquellen enthalten die erste Schrift, die das Dokument verwendet.
self.assertEqual(1, len(font_sources))
self.assertTrue(any([f.full_font_name == 'Arial' for f in font_sources[0].get_available_fonts()]))
# Die zweite Schrift, "Amethysta", ist nicht verfügbar.
self.assertFalse(any([f.full_font_name == 'Amethysta' for f in font_sources[0].get_available_fonts()]))
# Wir können eine Schrift-Ersetzungstabelle konfigurieren, die bestimmt
# welche Schriften Aspose.Words als Ersatz für nicht verfügbare Schriften verwendet.
# Legen Sie zwei Ersatzschriften für "Amethysta" fest: "Arvo" und "Courier New".
# Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words den zweiten Ersatz zu verwenden, und so weiter.
doc.font_settings = aw.fonts.FontSettings()
doc.font_settings.substitution_settings.table_substitution.set_substitutes('Amethysta', ['Arvo', 'Courier New'])
# "Amethysta" ist nicht verfügbar, und die Ersetzungsregel besagt, dass die erste zu verwendende Ersatzschrift "Arvo" ist.
self.assertFalse(any([f.full_font_name == 'Arvo' for f in font_sources[0].get_available_fonts()]))
# "Arvo" ist ebenfalls nicht verfügbar, aber "Courier New" ist es.
self.assertTrue(any([f.full_font_name == 'Courier New' for f in font_sources[0].get_available_fonts()]))
# Das Ausgabedokument zeigt den Text, der die Schrift "Amethysta" verwendet, formatiert mit "Courier New".
doc.save(file_name=ARTIFACTS_DIR + 'FontSettings.TableSubstitution.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

