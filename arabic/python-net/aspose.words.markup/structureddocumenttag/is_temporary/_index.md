---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /ar/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# أدرج وسم مستند مهيكل نص عادي،
# والذي سيعمل كنموذج نص عادي يمكن للمستخدم إدخال النص فيه.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# قم بتعيين الخاصية "IsTemporary" إلى "true" لجعل علامة المستند المهيكلة تختفي و
# ادمج محتواها في المستند بعد أن يقوم المستخدم بتحريره مرة واحدة في Microsoft Word.
# قم بتعيين الخاصية "IsTemporary" إلى "false" للسماح للمستخدم بتحرير المحتوى
# لعلامة المستند المهيكلة عددًا غير محدود من المرات.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# أدرج علامة مستند مهيكلة أخرى على شكل مربع اختيار وقم بتعيين حالتها الافتراضية إلى "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# قم بتعيين الخاصية "IsTemporary" إلى "true" لجعل مربع الاختيار يتحول إلى رمز
# بعد أن ينقر المستخدم عليه في Microsoft Word.
# قم بتعيين الخاصية "IsTemporary" إلى "false" للسماح للمستخدم بالنقر على مربع الاختيار عددًا غير محدود من المرات.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

