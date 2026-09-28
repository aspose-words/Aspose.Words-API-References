---
title: StructuredDocumentTag.placeholder_name property
linktitle: placeholder_name property
articleTitle: placeholder_name property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.placeholder_name property. Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text."
type: docs
weight: 240
url: /ar/python-net/aspose.words.markup/structureddocumenttag/placeholder_name/
---

## StructuredDocumentTag.placeholder_name property

Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.




```python
@property
def placeholder_name(self) -> str:
    ...

@placeholder_name.setter
def placeholder_name(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [Document.glossary_document](../../../aspose.words/document/glossary_document/). |

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# أدرج علامة مستند منظم بنص عادي من النوع \"PlainText\"، والتي ستعمل كصندوق نص.
# المحتوى الذي سيعرضه افتراضيًا هو موجه \"انقر هنا لإدخال النص.\"
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# يمكننا جعل العلامة تعرض محتويات كتلة بناء بدلاً من النص الافتراضي.
# أولاً، أضف كتلة بناء تحتوي على محتوى إلى مستند القاموس.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# ثم، استخدم خاصية \"PlaceholderName\" للعلامة المنظمة للمستند للإشارة إلى تلك كتلة البناء بالاسم.
tag.placeholder_name = 'Custom Placeholder'
# إذا كان \"PlaceholderName\" يشير إلى كتلة موجودة في مستند القاموس للوثيقة الأصلية،
# سوف نتمكن من التحقق من كتلة البناء عبر خاصية \"Placeholder\".
self.assertEqual(substitute_block, tag.placeholder)
# عيّن خاصية \"IsShowingPlaceholderText\" إلى \"true\" لتعامل الـ
# محتويات العلامة المنظمة للمستند الحالية كنص نائب.
# هذا يعني أن النقر على صندوق النص في Microsoft Word سيُبرز فورًا جميع محتويات العلامة.
# عيّن خاصية \"IsShowingPlaceholderText\" إلى \"false\" للحصول على الـ
# العلامة المنظمة للمستند لتعامل محتوياتها كنص أدخله المستخدم بالفعل.
# النقر على هذا النص في Microsoft Word سيضع المؤشر الوميض في الموقع الذي تم النقر عليه.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

