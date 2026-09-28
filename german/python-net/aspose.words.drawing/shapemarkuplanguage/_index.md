---
title: ShapeMarkupLanguage enumeration
linktitle: ShapeMarkupLanguage enumeration
articleTitle: ShapeMarkupLanguage enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShapeMarkupLanguage enumeration. Specifies Markup language used for the shape."
type: docs
weight: 390
url: /de/python-net/aspose.words.drawing/shapemarkuplanguage/
---

## ShapeMarkupLanguage enumeration

Specifies Markup language used for the shape.


### Members

| Name | Description |
| --- | --- |
| DML | Drawing Markup Language is used to define the shape. |
| VML | Vector Markup Language is used to define the shape. |

### Examples

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Wenn wir Kompatibilitätsoptionen konfigurieren, um Microsoft Word 2003 zu entsprechen,
# wird das Einfügen eines Bildes seine Form mithilfe von VML definieren.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# Die "ISO/IEC 29500:2008" OOXML-Standard unterstützt keine VML-Formen.
# Wenn wir die "Compliance"-Eigenschaft des SaveOptions-Objekts auf "OoxmlCompliance.Iso29500_2008_Strict" setzen,
# muss jedes Dokument, das wir speichern, während wir dieses Objekt übergeben, diesem Standard folgen.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Unser gespeichertes Dokument definiert die Form mithilfe von DML, um dem "ISO/IEC 29500:2008" OOXML-Standard zu entsprechen.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

### See Also

* module [aspose.words.drawing](../)

