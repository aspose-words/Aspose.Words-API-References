---
title: StructuredDocumentTag.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.title property. Specifies the friendly name associated with this SDT"
type: docs
weight: 290
url: /fr/python-net/aspose.words.markup/structureddocumenttag/title/
---

## StructuredDocumentTag.title property

Specifies the friendly name associated with this **SDT**.
Can not be ``None``.



```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# Créez une balise de document structuré qui contiendra du texte brut.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Définissez le titre et la couleur du cadre qui apparaît lorsque vous survolez la balise de document structuré dans Microsoft Word.
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# Définissez une balise pour cette balise de document structuré, qui est obtenable
# en tant qu'élément XML nommé "tag", avec la chaîne ci‑dessous dans son attribut "@val".
tag.tag = 'MyPlainTextSDT'
# Chaque balise de document structuré possède un ID unique aléatoire.
self.assertTrue(tag.id > 0)
# Définissez la police du texte à l'intérieur de la balise de document structuré.
tag.contents_font.name = 'Arial'
# Définissez la police du texte à la fin de la balise de document structuré.
# Tout texte que nous tapons dans le corps du document après être sortis de la balise avec les touches fléchées utilisera cette police.
tag.end_character_font.name = 'Arial Black'
# Par défaut, c'est faux et appuyer sur Entrée à l'intérieur d'une balise de document structuré ne fait rien.
# Lorsque défini sur vrai, notre balise de document structuré peut comporter plusieurs lignes.
# Définissez la propriété "Multiline" sur "false" pour n'autoriser que le contenu
# de cette balise de document structuré à s'étendre sur une seule ligne.
# Définissez la propriété "Multiline" sur "true" pour permettre à la balise de contenir plusieurs lignes de contenu.
tag.multiline = True
# Définissez la propriété "Appearance" sur "SdtAppearance.Tags" pour afficher des balises autour du contenu.
# Par défaut, la balise de document structuré s'affiche comme BoundingBox.
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# Insérez un clone de notre balise de document structuré dans un nouveau paragraphe.
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# Utilisez la méthode "RemoveSelfOnly" pour supprimer une balise de document structuré, tout en conservant son contenu dans le document.
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

