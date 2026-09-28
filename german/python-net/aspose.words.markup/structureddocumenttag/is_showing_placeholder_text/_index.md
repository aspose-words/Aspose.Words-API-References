---
title: StructuredDocumentTag.is_showing_placeholder_text property
linktitle: is_showing_placeholder_text property
articleTitle: is_showing_placeholder_text property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_showing_placeholder_text property. Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT)."
type: docs
weight: 150
url: /de/python-net/aspose.words.markup/structureddocumenttag/is_showing_placeholder_text/
---

## StructuredDocumentTag.is_showing_placeholder_text property

Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text
(as opposed to regular text contents within the SDT).


if set to ``True``, this state shall be resumed (showing placeholder text) upon opening this document.





```python
@property
def is_showing_placeholder_text(self) -> bool:
    ...

@is_showing_placeholder_text.setter
def is_showing_placeholder_text(self, value: bool):
    ...

```

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

