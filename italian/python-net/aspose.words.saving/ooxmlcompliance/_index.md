---
title: OoxmlCompliance enumeration
linktitle: OoxmlCompliance enumeration
articleTitle: OoxmlCompliance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.OoxmlCompliance enumeration. Allows to specify which OOXML specification will be used when saving in the DOCX format."
type: docs
weight: 550
url: /it/python-net/aspose.words.saving/ooxmlcompliance/
---

## OoxmlCompliance enumeration

Allows to specify which OOXML specification will be used when saving in the DOCX format.


### Members

| Name | Description |
| --- | --- |
| ECMA376_2006 | ECMA-376 1st Edition, 2006. |
| ISO29500_2008_TRANSITIONAL | ISO/IEC 29500:2008 Transitional compliance level. |
| ISO29500_2008_STRICT | ISO/IEC 29500:2008 Strict compliance level. |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Se configuriamo le opzioni di compatibilità per conformarci a Microsoft Word 2003,
# l'inserimento di un'immagine definirà la sua forma usando VML.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
# Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
# qualsiasi documento che salviamo passando questo oggetto dovrà rispettare quello standard.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Il nostro documento salvato definisce la forma usando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
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
# La proprietà "IsRestartAtEachSection" sarà applicabile solo quando
# il livello di conformità OOXML del documento è a uno standard più recente di "OoxmlComplianceCore.Ecma376".
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
# Di seguito sono riportati due tipi di avvolgimento che le forme possono avere.
# 1 -  Fluttuante:
builder.insert_shape(shape_type=aw.drawing.ShapeType.TOP_CORNERS_ROUNDED, horz_pos=aw.drawing.RelativeHorizontalPosition.PAGE, left=100, vert_pos=aw.drawing.RelativeVerticalPosition.PAGE, top=100, width=50, height=50, wrap_type=aw.drawing.WrapType.NONE)
# 2 -  In linea:
builder.insert_shape(shape_type=aw.drawing.ShapeType.DIAGONAL_CORNERS_ROUNDED, width=50, height=50)
# Se hai bisogno di creare forme "non-primitive", come SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
# TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, o DiagonalCornersRounded,
# allora salva il documento con conformità "Strict" o "Transitional", che consente di salvare la forma come DML.
save_options = aw.saving.OoxmlSaveOptions(aw.SaveFormat.DOCX)
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
doc.save(file_name=ARTIFACTS_DIR + 'Shape.ShapeInsertion.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

