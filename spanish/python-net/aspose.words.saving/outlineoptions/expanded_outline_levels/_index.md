---
title: OutlineOptions.expanded_outline_levels property
linktitle: expanded_outline_levels property
articleTitle: expanded_outline_levels property
second_title: Aspose.Words for Python
description: "OutlineOptions.expanded_outline_levels property. Specifies how many levels in the document outline to show expanded when the file is viewed."
type: docs
weight: 60
url: /es/python-net/aspose.words.saving/outlineoptions/expanded_outline_levels/
---

## OutlineOptions.expanded_outline_levels property

Specifies how many levels in the document outline to show expanded when the file is viewed.


```python
@property
def expanded_outline_levels(self) -> int:
    ...

@expanded_outline_levels.setter
def expanded_outline_levels(self, value: int):
    ...

```

### Remarks

Note that this options will not work when saving to XPS.

Specify 0 and the document outline will be collapsed; specify 1 and the first level items
in the outline will be expanded and so on.

Default is 0. Valid range is 0 to 9.




### Examples

Shows how to convert a whole document to PDF with three levels in the document outline.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Inserte encabezados de niveles 1 a 5.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
self.assertTrue(builder.paragraph_format.is_heading)
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 1.2.1')
builder.writeln('Heading 1.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 1.2.2.1')
builder.writeln('Heading 1.2.2.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING5
builder.writeln('Heading 1.2.2.2.1')
builder.writeln('Heading 1.2.2.2.2')
# Cree un objeto "PdfSaveOptions" que podamos pasar al método "Save" del documento
# para modificar cómo ese método convierte el documento a .PDF.
options = aw.saving.PdfSaveOptions()
# El documento PDF de salida contendrá un esquema, que es una tabla de contenidos que enumera los encabezados en el cuerpo del documento.
# Al hacer clic en una entrada de este esquema, nos llevará a la ubicación de su encabezado correspondiente.
# Establezca la propiedad "HeadingsOutlineLevels" a "4" para excluir todos los encabezados cuyos niveles estén por encima de 4 del esquema.
options.outline_options.headings_outline_levels = 4
# Si una entrada del esquema tiene entradas subsecuentes de un nivel superior entre ella y la siguiente entrada del mismo o nivel inferior,
# aparecerá una flecha a la izquierda de la entrada. Esta entrada es el "owner" de varias "sub-entries".
# En nuestro documento, las entradas del esquema del nivel de encabezado 5 son sub-entradas de la segunda entrada del esquema de nivel 4,
# las entradas de nivel de encabezado 4 y 5 son subentradas de la segunda entrada de nivel 3, y así sucesivamente.
# En el esquema, podemos hacer clic en la flecha de la entrada "owner" para contraer/expandir todas sus subentradas.
# Establezca la propiedad "ExpandedOutlineLevels" en "2" para expandir automáticamente todas las entradas de esquema de nivel de encabezado 2 y inferiores
# y contraer todas las entradas de nivel 3 y superiores al abrir el documento.
options.outline_options.expanded_outline_levels = 2
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExpandedOutlineLevels.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OutlineOptions](../)

