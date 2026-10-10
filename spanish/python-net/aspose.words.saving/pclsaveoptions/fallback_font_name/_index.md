---
title: PclSaveOptions.fallback_font_name property
linktitle: fallback_font_name property
articleTitle: fallback_font_name property
second_title: Aspose.Words for Python
description: "PclSaveOptions.fallback_font_name property. Name of the font that will be used if no expected font is found in printer and built-in fonts collections."
type: docs
weight: 20
url: /es/python-net/aspose.words.saving/pclsaveoptions/fallback_font_name/
---

## PclSaveOptions.fallback_font_name property

Name of the font that will be used
if no expected font is found in printer and built-in fonts collections.


```python
@property
def fallback_font_name(self) -> str:
    ...

@fallback_font_name.setter
def fallback_font_name(self, value: str):
    ...

```

### Remarks

If no fallback is found, a warning is generated and "Arial" font is used.


### Examples

Shows how to declare a font that a printer will apply to printed text as a substitute should its original font be unavailable.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Non-existent font'
builder.write('Hello world!')
save_options = aw.saving.PclSaveOptions()
save_options.fallback_font_name = 'Times New Roman'
# Este documento indicará a la impresora que aplique "Times New Roman" al texto con la fuente faltante.
# Si "Times New Roman" también no está disponible, la impresora usará por defecto la fuente "Arial".
doc.save(file_name=ARTIFACTS_DIR + 'PclSaveOptions.SetPrinterFont.pcl', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PclSaveOptions](../)

