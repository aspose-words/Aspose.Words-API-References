---
title: BuiltInDocumentProperties.hyperlink_base property
linktitle: hyperlink_base property
articleTitle: hyperlink_base property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.hyperlink_base property. Specifies the base string used for evaluating relative hyperlinks in this document."
type: docs
weight: 130
url: /ar/python-net/aspose.words.properties/builtindocumentproperties/hyperlink_base/
---

## BuiltInDocumentProperties.hyperlink_base property

Specifies the base string used for evaluating relative hyperlinks in this document.


```python
@property
def hyperlink_base(self) -> str:
    ...

@hyperlink_base.setter
def hyperlink_base(self, value: str):
    ...

```

### Remarks

Aspose.Words does not use this property.




### Examples

Shows how to store the base part of a hyperlink in the document's properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج ارتباطًا تشعبيًا نسبيًا إلى مستند في نظام الملفات المحلي يُسمى "Document.docx".
# النقر على الرابط في Microsoft Word سيفتح المستند المحدد، إذا كان متاحًا.
builder.insert_hyperlink('Relative hyperlink', 'Document.docx', False)
# هذا الرابط نسبي. إذا لم يكن هناك "Document.docx" في نفس المجلد
# كالوثيقة التي تحتوي على هذا الرابط، سيصبح الرابط معطلاً.
self.assertFalse(system_helper.io.File.exist(ARTIFACTS_DIR + 'Document.docx'))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.BrokenLink.docx')
# الوثيقة التي نحاول الارتباط بها موجودة في دليل مختلف عن الدليل الذي نخطط لحفظ الوثيقة فيه.
# يمكننا إصلاح الروابط بهذه الطريقة عن طريق وضع اسم ملف مطلق في كل منها.
# بدلاً من ذلك، يمكننا توفير رابط أساسي يضيفه كل ارتباط تشعبي يحتوي على اسم ملف نسبي
# سيُسبق إلى رابطه عندما نضغط عليه.
properties = doc.built_in_document_properties
properties.hyperlink_base = MY_DIR
self.assertTrue(system_helper.io.File.exist(properties.hyperlink_base + doc.range.fields[0].as_field_hyperlink().address))
doc.save(file_name=ARTIFACTS_DIR + 'DocumentProperties.HyperlinkBase.WorkingLink.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

