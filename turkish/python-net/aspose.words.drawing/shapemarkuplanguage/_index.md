---
title: ShapeMarkupLanguage enumeration
linktitle: ShapeMarkupLanguage enumeration
articleTitle: ShapeMarkupLanguage enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.ShapeMarkupLanguage enumeration. Specifies Markup language used for the shape."
type: docs
weight: 390
url: /tr/python-net/aspose.words.drawing/shapemarkuplanguage/
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
# Microsoft Word 2003 ile uyumlu olacak şekilde uyumluluk seçeneklerini yapılandırırsak,
# bir görüntü eklemek, şekilini VML kullanarak tanımlayacaktır.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2003)
builder.insert_image(file_name=IMAGE_DIR + 'Transparent background logo.png')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.VML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
# Bu "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
# Eğer SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
# Bu nesneyi geçirerek kaydettiğimiz herhangi bir belge o standarda uymak zorunda kalacaktır.
save_options = aw.saving.OoxmlSaveOptions()
save_options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_STRICT
save_options.save_format = aw.SaveFormat.DOCX
doc.save(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx', save_options=save_options)
# Kaydedilen belgemiz şekli DML kullanarak tanımlar ve "ISO/IEC 29500:2008" OOXML standardına uyar.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'OoxmlSaveOptions.Iso29500Strict.docx')
self.assertEqual(aw.drawing.ShapeMarkupLanguage.DML, doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape().markup_language)
```

### See Also

* module [aspose.words.drawing](../)

