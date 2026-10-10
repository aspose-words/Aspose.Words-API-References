---
title: DocumentBuilder.is_at_end_of_structured_document_tag property
linktitle: is_at_end_of_structured_document_tag property
articleTitle: is_at_end_of_structured_document_tag property
second_title: Aspose.Words for Python
description: "DocumentBuilder.is_at_end_of_structured_document_tag property. Returns true if the cursor is at the end of a structured document tag."
type: docs
weight: 120
url: /it/python-net/aspose.words/documentbuilder/is_at_end_of_structured_document_tag/
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
# Ci sono diversi modi per spostare il cursore:
# 1 -  Spostati al primo carattere del tag di documento strutturato per indice.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=1)
# 2 -  Spostati al primo carattere del tag di documento strutturato per oggetto.
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG, 2, True).as_structured_document_tag()
builder.move_to_structured_document_tag(structured_document_tag=tag, character_index=1)
builder.write(' New text.')
self.assertEqual('R New text.ichText', tag.get_text().strip())
# 3 -  Spostati alla fine del secondo tag di documento strutturato.
builder.move_to_structured_document_tag(structured_document_tag_index=1, character_index=-1)
self.assertTrue(builder.is_at_end_of_structured_document_tag)
# Ottieni il tag di documento strutturato attualmente selezionato.
builder.current_structured_document_tag.color = aspose.pydrawing.Color.green
doc.save(file_name=ARTIFACTS_DIR + 'Document.MoveToStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

