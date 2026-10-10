---
title: DocumentBuilder.is_at_end_of_structured_document_tag property
linktitle: is_at_end_of_structured_document_tag property
articleTitle: is_at_end_of_structured_document_tag property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_structured_document_tag property. Returns true if the cursor is at the end of a structured document tag."
type: docs
weight: 120
url: /sv/python-net/aspose.words/documentbuilder/is_at_end_of_structured_document_tag/
---

## DocumentBuilder.is_at_end_of_structured_document_tag property

Returns **true** if the cursor is at the end of a structured document tag.



```python
@property
def is_at_end_of_structured_document_tag(self) -> bool:
    ...

```

### Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Structured document tags.docx')
builder = aw.DocumentBuilder(doc=doc)
# Det finns flera sätt att flytta markören:
# 1 -  Flytta till det första tecknet i strukturerad dokumenttagg efter index.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=1)
# 2 -  Flytta till det första tecknet i strukturerad dokumenttagg efter objekt.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(structured_document_tag=tag, character_index=1)
builder.write(' New text.')
self.assertEqual('R New text.ichText', tag.get_text().strip())
# 3 -  Flytta till slutet av den andra strukturerade dokumenttaggen.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=-1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)
# Hämta för närvarande markerad strukturerad dokumenttagg.
builder.current_structured_document_tag.color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Document.MoveToStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

