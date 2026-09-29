---
title: OoxmlSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compliance property. Specifies the OOXML version for the output document"
type: docs
weight: 20
url: /es/python-net/aspose.words.saving/ooxmlsaveoptions/compliance/
---

## OoxmlSaveOptions.compliance property

Specifies the OOXML version for the output document.
The default value is [OoxmlCompliance.ECMA376_2006](../../ooxmlcompliance/#ECMA376_2006).



```python
@property
def compliance(self) -> aspose.words.saving.OoxmlCompliance:
    ...

@compliance.setter
def compliance(self, value: aspose.words.saving.OoxmlCompliance):
    ...

```

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Si configuramos opciones de compatibilidad para cumplir con Microsoft Word 2003,
# insertar una imagen definirá su forma usando VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# The estándar "ISO/IEC 29500:2008" OOXML no admite formas VML.
# Si establecemos la propiedad "Compliance" del objeto SaveOptions a "OoxmlCompliance.Iso29500_2008_Strict",
# cualquier documento que guardemos pasando este objeto deberá seguir ese estándar.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Nuestro documento guardado define la forma usando DML para cumplir con el estándar "ISO/IEC 29500:2008" OOXML.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

Shows how to configure a list to restart numbering at each section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
doc_list = doc.lists[0]
doc_list.is_restart_at_each_section = restart_list_at_each_section
# La propiedad "IsRestartAtEachSection" solo será aplicable cuando
# el nivel de cumplimiento OOXML del documento sea un estándar más reciente que "OoxmlComplianceCore.Ecma376".
options = aw.saving.OoxmlSaveOptions()
options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
builder.list_format.list = doc_list
builder.writeln('List item 1')
builder.writeln('List item 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('List item 3')
builder.writeln('List item 4')
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.RestartingDocumentList.docx', save_options=options)
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.RestartingDocumentList.docx')
self.assertEqual(restart_list_at_each_section, doc.lists[0].is_restart_at_each_section)
```

Shows how to insert DML shapes into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# A continuación se presentan dos tipos de ajuste que pueden tener las formas.
# 1 -  Flotante:
builder.insert_shape(shape_type=aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, horz_pos=aw.drawing.RelativeHorizontalPosition.PAGE, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.PAGE, top=100, width=50, height=50, wrap_type=aw.drawing.WrapType.NONE)
# 2 -  En línea:
builder.insert_shape(shape_type=aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, width=50, height=50)
# Si necesita crear formas "non-primitive", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
# entonces guarde el documento con cumplimiento "Strict" o "Transitional", lo que permite guardar la forma como DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ShapeInsertion.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

