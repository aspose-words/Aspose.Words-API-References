---
title: DocumentBuilder.current_structured_document_tag property
linktitle: current_structured_document_tag property
articleTitle: current_structured_document_tag property
second_title: Aspose.Words for Python
description: "DocumentBuilder.current_structured_document_tag property. Gets the structured document tag that is currently selected in this [DocumentBuilder](../)."
type: docs
weight: 80
url: /ar/python-net/aspose.words/documentbuilder/current_structured_document_tag/
---

## DocumentBuilder.current_structured_document_tag property

Gets the structured document tag that is currently selected in this [DocumentBuilder](../).



```python
@property
def current_structured_document_tag(self) -> aspose.words.markup.StructuredDocumentTag:
    ...

```

### Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
builder = aw.DocumentBuilder(doc=doc)
# هناك عدة طرق لتحريك المؤشر:
# 1 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الفهرس.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=1)
# 2 -  الانتقال إلى الحرف الأول لعلامة المستند المهيكلة حسب الكائن.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(structured_document_tag=tag, character_index=1)
builder.write(' New text.')
self.assertEqual('R New text.ichText', tag.get_text().strip())
# 3 -  الانتقال إلى نهاية علامة المستند المهيكلة الثانية.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=-1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)
# احصل على علامة المستند المهيكلة المحددة حاليًا.
builder.current_structured_document_tag.color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Document.MoveToStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

