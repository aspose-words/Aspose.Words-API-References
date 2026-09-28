---
title: StructuredDocumentTag.placeholder property
linktitle: placeholder property
articleTitle: placeholder property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.placeholder property. Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTag.xml_mapping](../xml_mapping/) element or the [StructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is ``True``."
type: docs
weight: 230
url: /de/python-net/aspose.words.markup/structureddocumenttag/placeholder/
---

## StructuredDocumentTag.placeholder property

Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty,
the associated mapped XML element is empty as specified via the [StructuredDocumentTag.xml_mapping](../xml_mapping/) element
or the [StructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is ``True``.



```python
@property
def placeholder(self) -> aspose.words.buildingblocks.BuildingBlock:
    ...

```

### Remarks

Can be ``None``, meaning that the placeholder is not applicable for this Sdt.


### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Fügen Sie ein strukturiertes Dokument-Tag des Typs "PlainText" für Klartext ein, das als Textfeld fungiert.
# Der Inhalt, den es standardmäßig anzeigt, ist die Eingabeaufforderung "Click here to enter text.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Wir können das Tag dazu bringen, den Inhalt eines Bausteins anstelle des Standardtexts anzuzeigen.
# Fügen Sie zunächst einen Baustein mit Inhalt zum Glossar-Dokument hinzu.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Verwenden Sie dann die Eigenschaft "PlaceholderName" des strukturierten Dokument-Tags, um diesen Baustein per Namen zu referenzieren.
tag.placeholder_name = 'Custom Placeholder'
# Wenn sich "PlaceholderName" auf einen vorhandenen Block im Glossar-Dokument des übergeordneten Dokuments bezieht,
# können wir den Baustein über die Eigenschaft "Placeholder" verifizieren.
self.assertEqual(substitute_block, tag.placeholder)
# Setzen Sie die Eigenschaft "IsShowingPlaceholderText" auf "true", um das
# den aktuellen Inhalt des strukturierten Dokument-Tags als Platzhaltertext zu behandeln.
# Das bedeutet, dass ein Klick auf das Textfeld in Microsoft Word sofort den gesamten Inhalt des Tags hervorhebt.
# Setzen Sie die Eigenschaft "IsShowingPlaceholderText" auf "false", um das
# strukturierte Dokument-Tag dazu zu bringen, seinen Inhalt als bereits vom Benutzer eingegebenen Text zu behandeln.
# Ein Klick auf diesen Text in Microsoft Word positioniert den blinkenden Cursor an der angeklickten Stelle.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

