---
title: IStructuredDocumentTag.placeholder_name property
linktitle: placeholder_name property
articleTitle: placeholder_name property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.placeholder_name property. Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text."
type: docs
weight: 110
url: /sv/python-net/aspose.words.markup/istructureddocumenttag/placeholder_name/
---

## IStructuredDocumentTag.placeholder_name property

Gets or sets Name of the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text.




```python
@property
def placeholder_name(self) -> str:
    ...

@placeholder_name.setter
def placeholder_name(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if BuildingBlock with this name [BuildingBlock.name](../../../aspose.words.buildingblocks/buildingblock/name/) is not present in [Document.glossary_document](../../../aspose.words/document/glossary_document/). |

### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Infoga en strukturerad dokumenttagg av typen "PlainText" med vanlig text, som kommer att fungera som en textruta.
# Innehållet som den visar som standard är en uppmaning "Click here to enter text.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Vi kan få taggen att visa innehållet i ett byggblock istället för standardtexten.
# Först, lägg till ett byggblock med innehåll i glossariedokumentet.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Använd sedan den strukturerade dokumenttaggens egenskap "PlaceholderName" för att referera till det byggblocket med namn.
tag.placeholder_name = 'Custom Placeholder'
# Om "PlaceholderName" refererar till ett befintligt block i förälderdokumentets glossariedokument,
# kommer vi att kunna verifiera byggblocket via egenskapen "Placeholder".
self.assertEqual(substitute_block, tag.placeholder)
# Ställ in egenskapen "IsShowingPlaceholderText" till "true" för att behandla
# den strukturerade dokumenttaggens aktuella innehåll som platshållartext.
# Detta betyder att ett klick på textrutan i Microsoft Word omedelbart markerar hela taggens innehåll.
# Ställ in egenskapen "IsShowingPlaceholderText" till "false" för att få
# den strukturerade dokumenttaggen att behandla dess innehåll som text som en användare redan har skrivit in.
# Att klicka på den här texten i Microsoft Word placerar den blinkande markören på den klickade platsen.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

