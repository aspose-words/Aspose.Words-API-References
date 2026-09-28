---
title: StructuredDocumentTag.clear method
linktitle: clear method
articleTitle: clear method
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.clear method. Clears contents of this structured document tag and displays a placeholder if it is defined."
type: docs
weight: 360
url: /fr/python-net/aspose.words.markup/structureddocumenttag/clear/
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
# Créez une balise de document structuré en texte brut, puis ajoutez‑la au document.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.BLOCK)
doc.first_section.body.append_child(tag)
# Cette balise de document structuré, qui est sous forme de zone de texte, affiche déjà un texte d'espace réservé.
self.assertEqual('Click here to enter text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# Créez un bloc de construction avec du texte.
glossary_doc = doc.glossary_document
substitute_block = aw.buildingblocks.BuildingBlock(glossary_doc)
substitute_block.name = 'My placeholder'
substitute_block.append_child(aw.Section(glossary_doc))
substitute_block.first_section.ensure_minimum()
substitute_block.first_section.body.first_paragraph.append_child(aw.Run(doc=glossary_doc, text='Custom placeholder text.'))
glossary_doc.append_child(substitute_block)
# Définissez la propriété "PlaceholderName" de la balise de document structuré sur le nom de notre bloc de construction pour obtenir
# la balise de document structuré affichant le contenu du bloc de construction à la place du texte par défaut original.
tag.placeholder_name = 'My placeholder'
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
self.assertTrue(tag.is_showing_placeholder_text)
# Modifiez le texte de la balise de document structuré et masquez le texte d'espace réservé.
run = tag.get_child(aw.NodeType.RUN, 0, True).as_run()
run.text = 'New text.'
tag.is_showing_placeholder_text = False
self.assertEqual('New text.', tag.get_text().strip())
# Utilisez la méthode "Clear" pour effacer le contenu de cette balise de document structuré et afficher à nouveau l'espace réservé.
tag.clear()
self.assertTrue(tag.is_showing_placeholder_text)
self.assertEqual('Custom placeholder text.', tag.get_text().strip())
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

