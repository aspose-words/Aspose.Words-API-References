---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /es/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Cree un objeto "RtfSaveOptions" para pasar al método "Save" del documento y modificar cómo lo guardamos en un RTF.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# Establezca la propiedad "ExportCompactSize" a "true" para
# reducir el tamaño del documento guardado a costa de la compatibilidad con texto de derecha a izquierda.
options.export_compact_size = True
# Establezca la propiedad "ExportImagesFotOldReaders" a "true" para usar palabras clave adicionales y asegurar que nuestro documento sea
# compatible con lectores pre-Microsoft Word 97 y WordPad.
# Establezca la propiedad "ExportImagesFotOldReaders" a "false" para reducir el tamaño del documento,
# pero evitar que los lectores antiguos puedan leer cualquier imagen que no sea metafile o BMP que el documento pueda contener.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

