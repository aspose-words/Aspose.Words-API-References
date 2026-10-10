---
title: OoxmlSaveOptions.compliance property
linktitle: compliance property
articleTitle: compliance property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.compliance property. Specifies the OOXML version for the output document"
type: docs
weight: 20
url: /fr/python-net/aspose.words.saving/ooxmlsaveoptions/compliance/
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
# Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
# l'insertion d'une image définira sa forme à l'aide de VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# Le "ISO/IEC 29500:2008" standard OOXML ne prend pas en charge les formes VML.
# Si nous définissons la propriété "Compliance" de l'objet SaveOptions sur "OoxmlCompliance.Iso29500_2008_Strict",
# tout document que nous enregistrons en passant cet objet devra suivre ce standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Notre document enregistré définit la forme en utilisant DML pour se conformer au standard "ISO/IEC 29500:2008" OOXML.
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
# La propriété "IsRestartAtEachSection" ne sera applicable que lorsque
# le niveau de conformité OOXML du document correspond à un standard plus récent que "OoxmlComplianceCore.Ecma376".
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
# Ci-dessous, deux types d'enveloppage que les formes peuvent avoir.
# 1 -  Flottant :
builder.insert_shape(shape_type=aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, horz_pos=aw.drawing.RelativeHorizontalPosition.PAGE, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.PAGE, top=100, width=50, height=50, wrap_type=aw.drawing.WrapType.NONE)
# 2 -  En ligne :
builder.insert_shape(shape_type=aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, width=50, height=50)
# Si vous devez créer des formes "non-primitive", telles que SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, ou DiagonalCornersRounded,
# alors enregistrez le document avec la conformité "Strict" ou "Transitional", ce qui permet d'enregistrer la forme en tant que DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ShapeInsertion.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

