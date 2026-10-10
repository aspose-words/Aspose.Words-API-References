---
title: StructuredDocumentTag.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.id property. Specifies a unique read-only persistent numerical Id for this SDT."
type: docs
weight: 140
url: /ar/python-net/aspose.words.markup/structureddocumenttag/id/
---

## StructuredDocumentTag.id property

Specifies a unique read-only persistent numerical Id for this **SDT**.




```python
@property
def id(self) -> int:
    ...

```

### Remarks

Id attribute shall follow these rules:

* The document shall retain SDT ids only if the whole document is cloned [Document.clone()](../../../aspose.words/document/clone/#bool).
  
* During [DocumentBase.import_node()](../../../aspose.words/documentbase/import_node/#node_bool)
  Id shall be retained if import does not cause conflicts with other SDT Ids in
  the target document.
  
* If multiple SDT nodes specify the same decimal number value for the Id attribute,
  then the first SDT in the document shall maintain this original Id,
  and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
  
* During standalone SDT Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener) operation new unique ID will be generated for the cloned SDT node.
  
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned
  to it when the document is loaded.
  





### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# أنشئ علامة مستند منظم ستحتوي على نص عادي.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# عيّن عنوان وإلوان الإطار الذي يظهر عندما تمرّر الفأرة فوق العلامة المنظمة للمستند في Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# قم بتعيين علامة لهذا الوسم المهيكل للمستند، والتي يمكن الحصول عليها
# كعنصر XML يُسمى "tag"، مع السلسلة أدناه في خاصية "@val" الخاصة به.
tag.tag = 'MyPlainTextSDT'
# كل وسم مهيكل للمستند لديه معرف فريد عشوائي.
self.assertTrue(tag.id > 0)
# قم بتعيين الخط للنص داخل وسم المستند المهيكل.
tag.contents_font.name = 'Arial'
# قم بتعيين الخط للنص في نهاية وسم المستند المهيكل.
# أي نص نكتبه في جسم المستند بعد الخروج من الوسم باستخدام مفاتيح السهم سيستخدم هذا الخط.
tag.end_character_font.name = 'Arial Black'
# بشكل افتراضي، هذه القيمة خاطئة وعند الضغط على Enter داخل وسم المستند المهيكل لا يحدث شيء.
# عند تعيينها إلى true، يمكن لوسم المستند المهيكل أن يحتوي على عدة أسطر.
# قم بتعيين الخاصية "Multiline" إلى "false" للسماح فقط بالمحتويات
# لوسم المستند المهيكل هذا لتقع في سطر واحد.
# قم بتعيين الخاصية "Multiline" إلى "true" للسماح للوسم باحتواء عدة أسطر من المحتوى.
tag.multiline = True
# قم بتعيين الخاصية "Appearance" إلى "SdtAppearance.Tags" لإظهار الوسوم حول المحتوى.
# بشكل افتراضي، يظهر وسم المستند المهيكل كصندوق حدود (BoundingBox).
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# أدرج نسخة مستنسخة من وسم المستند المهيكل في فقرة جديدة.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# استخدم الطريقة "RemoveSelfOnly" لإزالة وسم المستند المهيكل، مع الحفاظ على محتوياته في المستند.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

