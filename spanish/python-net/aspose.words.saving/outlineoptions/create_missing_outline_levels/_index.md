---
title: OutlineOptions.create_missing_outline_levels property
linktitle: create_missing_outline_levels property
articleTitle: create_missing_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.create_missing_outline_levels property. Gets or sets a value determining whether or not to create missing outline levels when the document is  exported."
type: docs
weight: 30
url: /es/python-net/aspose.words.saving/outlineoptions/create_missing_outline_levels/
---

## OutlineOptions.create_missing_outline_levels property

Gets or sets a value determining whether or not to create missing outline levels when the document is 
exported.

Default value for this property is ``False``.




```python
@property
def create_missing_outline_levels(self) -> bool:
    ...

@create_missing_outline_levels.setter
def create_missing_outline_levels(self, value: bool):
    ...

```

### Examples

Shows how to work with outline levels that do not contain any corresponding headings when saving a PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte encabezados que puedan servir como entradas del índice (TOC) de niveles 1 y 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.1.1.1.1')
builder.writeln('Heading 1.1.1.1.2')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
save_options = aw.saving.PdfSaveOptions()
# El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
# Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su encabezado correspondiente.
# Establezca la propiedad "HeadingsOutlineLevels" en "5" para incluir todos los encabezados de nivel 5 y inferiores en el esquema.
save_options.outline_options.headings_outline_levels = 5
# Este documento contiene encabezados de los niveles 1 y 5, y no hay encabezados con niveles 2, 3 y 4.
# El documento PDF de salida tratará los niveles de esquema 2, 3 y 4 como "faltantes".
# Establezca la propiedad "CreateMissingOutlineLevels" en "true" para incluir todos los niveles faltantes en el esquema,
# dejando entradas de esquema en blanco ya que no hay encabezados utilizables.
# Establezca la propiedad "CreateMissingOutlineLevels" en "false" para ignorar los niveles de esquema faltantes,
# y trate los encabezados de nivel 5 del esquema como nivel 2.
save_options.outline_options.create_missing_outline_levels = create_missing_outline_levels
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.CreateMissingOutlineLevels.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

