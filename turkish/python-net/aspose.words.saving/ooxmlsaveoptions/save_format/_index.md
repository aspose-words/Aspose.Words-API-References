---
title: OoxmlSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 70
url: /tr/python-net/aspose.words.saving/ooxmlsaveoptions/save_format/
---

## OoxmlSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can be [SaveFormat.DOCX](../../../aspose.words/saveformat/#DOCX), [SaveFormat.DOCM](../../../aspose.words/saveformat/#DOCM),
[SaveFormat.DOTX](../../../aspose.words/saveformat/#DOTX), [SaveFormat.DOTM](../../../aspose.words/saveformat/#DOTM) or [SaveFormat.FLAT_OPC](../../../aspose.words/saveformat/#FLAT_OPC).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

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

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)

