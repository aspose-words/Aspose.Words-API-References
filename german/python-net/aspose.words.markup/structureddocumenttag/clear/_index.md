---
title: StructuredDocumentTag.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.clear method. Clears contents of this structured document tag and displays a placeholder if it is defined."
type: docs
weight: 360
url: /de/python-net/aspose.words.markup/structureddocumenttag/clear/
---

## clear() {#default}

Clears contents of this structured document tag and displays a placeholder if it is defined.


```python
def clear(self):
    ...
```

### Remarks

It is not possible to clear contents of a structured document tag if it has revisions.

If this structured document tag is mapped to custom XML (with using the [StructuredDocumentTag.xml_mapping](../xml_mapping/)
property), the referenced XML node is cleared.




### Examples

Shows how to delete contents of structured document tag elements.

```python
doc = aw.Document()
# Erstellen Sie ein strukturiertes Dokument-Tag für Klartext und fügen Sie es anschließend dem Dokument hinzu.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)
# Dieses strukturierte Dokument-Tag, das in Form einer Textbox vorliegt, zeigt bereits Platzhaltertext an.
self.assertEqual('Click here to enter text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# Erstellen Sie einen Baustein mit Textinhalt.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'My placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.ensure_minimum()
substitute_block.first_section.body.first_paragraph.append_child(aw.Run(doc=glossary_doc, text='Custom placeholder text.'))
glossary_doc.append_child(substitute_block)
# Setzen Sie die Eigenschaft "PlaceholderName" des strukturierten Dokument-Tags auf den Namen unseres Bausteins, um
# das strukturierte Dokument-Tag dazu zu bringen, den Inhalt des Bausteins anstelle des ursprünglichen Standardtexts anzuzeigen.
tag.placeholder_name = 'My placeholder'
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# Bearbeiten Sie den Text des strukturierten Dokument-Tags und blenden Sie den Platzhaltertext aus.
run = tag.get_child(aw.NodeType.RUN, 0, True).as_run()
run.text = 'New text.'
tag.is_showing_placeholder_text = False
self.assertEqual('New text.', tag.get_text().strip())
# Verwenden Sie die Methode "Clear", um den Inhalt dieses strukturierten Dokument-Tags zu leeren und den Platzhalter erneut anzuzeigen.
tag.clear()
self.assertTrue(tag.is_showing_placeholder_text)
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

