---
title: StructuredDocumentTag.is_temporary property
linktitle: is_temporary property
articleTitle: is_temporary property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.is_temporary property. Specifies whether this SDT shall be removed from the WordProcessingML document when its contents are modified."
type: docs
weight: 160
url: /fr/python-net/aspose.words.markup/structureddocumenttag/is_temporary/
---

## StructuredDocumentTag.is_temporary property

Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents
are modified.



```python
@property
def is_temporary(self) -> bool:
    ...

@is_temporary.setter
def is_temporary(self, value: bool):
    ...

```

### Examples

Shows how to make single-use controls.

```python
doc = aw.Document()
# Insérez une balise de document structuré en texte brut,
# qui servira de formulaire en texte brut dans lequel l'utilisateur pourra saisir du texte.
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# Définissez la propriété "IsTemporary" sur "true" pour faire disparaître la balise de document structuré et
# assimilez son contenu dans le document après que l'utilisateur l'ait modifié une fois dans Microsoft Word.
# Définissez la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de modifier le contenu
# de la balise de document structuré un nombre quelconque de fois.
tag.is_temporary = is_temporary
builder = aw.DocumentBuilder(doc=doc)
builder.write('Please enter text: ')
builder.insert_node(tag)
# Insérez une autre balise de document structuré sous forme de case à cocher et définissez son état par défaut sur "checked".
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
tag.checked = True
# Définissez la propriété "IsTemporary" sur "true" pour que la case à cocher devienne un symbole
# une fois que l'utilisateur clique dessus dans Microsoft Word.
# Définissez la propriété "IsTemporary" sur "false" pour permettre à l'utilisateur de cliquer sur la case à cocher un nombre quelconque de fois.
tag.is_temporary = is_temporary
builder.write('\nPlease click the check box: ')
builder.insert_node(tag)
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.IsTemporary.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

