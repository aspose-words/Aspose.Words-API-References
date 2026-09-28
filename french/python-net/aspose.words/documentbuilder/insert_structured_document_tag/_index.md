---
title: DocumentBuilder.insert_structured_document_tag method
linktitle: insert_structured_document_tag method
articleTitle: insert_structured_document_tag method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_structured_document_tag method. Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document."
type: docs
weight: 480
url: /fr/python-net/aspose.words/documentbuilder/insert_structured_document_tag/
---

## insert_structured_document_tag(type) {#sdttype}

Inserts a [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) into the document.



```python
def insert_structured_document_tag(self, type: aspose.words.markup.SdtType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | [SdtType](../../../aspose.words.markup/sdttype/) |  |

### Returns

The [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) node that was just inserted.


### Examples

Shows how to simply insert structured document tag.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to(doc.first_section.body.paragraphs[3])
# Remarque, seuls les types StructuredDocumentTag suivants sont autorisés pour l'insertion :
# SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
# SdtType.ComboBox, SdtType.Picture, SdtType.Date.
# Le niveau de balisage du StructuredDocumentTag inséré sera détecté automatiquement et dépend de la position d'insertion.
# Le StructuredDocumentTag ajouté héritera du formatage du paragraphe et de la police depuis la position du curseur.
sdt_plain = builder.insert_structured_document_tag(aw.markup.SdtType.PLAIN_TEXT)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.InsertStructuredDocumentTag.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

