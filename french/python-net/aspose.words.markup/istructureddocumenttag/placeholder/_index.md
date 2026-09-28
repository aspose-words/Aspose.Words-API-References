---
title: IStructuredDocumentTag.placeholder property
linktitle: placeholder property
articleTitle: placeholder property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.placeholder property. Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty,  the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xml_mapping](../xml_mapping/) element or the [IStructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is true."
type: docs
weight: 100
url: /fr/python-net/aspose.words.markup/istructureddocumenttag/placeholder/
---

## IStructuredDocumentTag.placeholder property

Gets the [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, 
the associated mapped XML element is empty as specified via the [IStructuredDocumentTag.xml_mapping](../xml_mapping/) element
or the [IStructuredDocumentTag.is_showing_placeholder_text](../is_showing_placeholder_text/) element is true. 



```python
@property
def placeholder(self) -> aspose.words.buildingblocks.BuildingBlock:
    ...

```

### Remarks

Can be null, meaning that the placeholder is not applicable for this Sdt.


### Examples

Shows how to use a building block's contents as a custom placeholder text for a structured document tag.

```python
doc = aw.Document()
# Insérez une balise de document structuré en texte brut du type "PlainText", qui fonctionnera comme une zone de texte.
# Le contenu qu'elle affichera par défaut est l'invite "Cliquez ici pour entrer du texte.".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Nous pouvons faire en sorte que la balise affiche le contenu d'un bloc de construction au lieu du texte par défaut.
# Tout d'abord, ajoutez un bloc de construction avec du contenu au document de glossaire.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'Custom Placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.append_child(aw.Body(glossary_doc))
substitute_block.first_section.body.append_paragraph('Custom placeholder text.')
glossary_doc.append_child(substitute_block)
# Ensuite, utilisez la propriété "PlaceholderName" de la balise de document structuré pour référencer ce bloc de construction par son nom.
tag.placeholder_name = 'Custom Placeholder'
# Si "PlaceholderName" fait référence à un bloc existant dans le document de glossaire du document parent,
# nous pourrons vérifier le bloc de construction via la propriété "Placeholder".
self.assertEqual(substitute_block, tag.placeholder)
# Définissez la propriété "IsShowingPlaceholderText" sur "true" pour traiter le
# contenu actuel de la balise de document structuré comme texte de substitution.
# Cela signifie que cliquer sur la zone de texte dans Microsoft Word mettra immédiatement en surbrillance tout le contenu de la balise.
# Définissez la propriété "IsShowingPlaceholderText" sur "false" pour obtenir le
# balise de document structuré afin qu'elle traite son contenu comme du texte déjà saisi par l'utilisateur.
# Cliquer sur ce texte dans Microsoft Word placera le curseur clignotant à l'endroit cliqué.
tag.is_showing_placeholder_text = is_showing_placeholder_text
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlaceholderBuildingBlock.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

