---
title: IStructuredDocumentTag.is_showing_placeholder_text property
linktitle: is_showing_placeholder_text property
articleTitle: is_showing_placeholder_text property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.is_showing_placeholder_text property. Specifies whether the content of this SDT shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT)."
type: docs
weight: 50
url: /it/python-net/aspose.words.markup/istructureddocumenttag/is_showing_placeholder_text/
---

## IStructuredDocumentTag.is_showing_placeholder_text property

Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text
(as opposed to regular text contents within the SDT). 


if set to true, this state shall be resumed (showing placeholder text) upon opening this document.




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
# Inserisci un tag di documento strutturato di testo semplice del tipo "PlainText", che funzionerà come una casella di testo.
# Il contenuto che visualizzerà per impostazione predefinita è un prompt "Click here to enter text.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Possiamo fare in modo che il tag visualizzi il contenuto di un blocco di costruzione invece del testo predefinito.
# Prima, aggiungi un blocco di costruzione con contenuti al documento glossario.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Quindi, usa la proprietà "PlaceholderName" del tag di documento strutturato per fare riferimento a quel blocco di costruzione per nome.
tag.placeholder_name = 'Custom Placeholder'
# Se "PlaceholderName" si riferisce a un blocco esistente nel documento glossario del documento principale,
# potremo verificare il blocco di costruzione tramite la proprietà "Placeholder".
self.assertEqual(substitute_block, tag.placeholder)
# Imposta la proprietà "IsShowingPlaceholderText" su "true" per trattare il
# contenuto attuale del tag di documento strutturato come testo segnaposto.
# Ciò significa che facendo clic sulla casella di testo in Microsoft Word verrà immediatamente evidenziato tutto il contenuto del tag.
# Imposta la proprietà "IsShowingPlaceholderText" su "false" per ottenere il
# tag di documento strutturato per trattare il suo contenuto come testo già inserito dall'utente.
# Facendo clic su questo testo in Microsoft Word il cursore lampeggiante verrà posizionato nella posizione cliccata.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

