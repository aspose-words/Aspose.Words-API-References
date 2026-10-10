---
title: XpsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 50
url: /es/python-net/aspose.words.saving/xpssaveoptions/save_format/
---

## XpsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to limit the headings' level that will appear in the outline of a saved XPS document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte encabezados que puedan servir como entradas del índice (TOC) de niveles 1, 2 y luego 3.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
# Cree un objeto "XpsSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .XPS.
save_options = aw.saving.XpsSaveOptions()
self.assertEqual(aw.SaveFormat.XPS, save_options.save_format)
# El documento XPS de salida contendrá un esquema, una tabla de contenido que enumera los encabezados en el cuerpo del documento.
# Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su encabezado correspondiente.
# Establezca la propiedad "HeadingsOutlineLevels" a "2" para excluir del esquema todos los encabezados cuyo nivel sea superior a 2.
# Los dos últimos encabezados que hemos insertado arriba no aparecerán.
save_options.outline_options.headings_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OutlineLevels.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

