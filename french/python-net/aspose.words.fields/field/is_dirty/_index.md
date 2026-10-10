---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /fr/python-net/aspose.words.fields/field/is_dirty/
---

## Field.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Donnez la valeur de la propriété intégrée "Author" du document, puis affichez‑la avec un champ.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Mettez à jour la propriété. Le champ affiche toujours l'ancienne valeur.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Comme la valeur du champ est obsolète, nous pouvons la marquer comme "dirty".
# Cette valeur restera obsolète jusqu'à ce que nous mettions à jour le champ manuellement avec la méthode Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Si nous enregistrons sans appeler de méthode de mise à jour,
    # le champ continuera d'afficher la valeur obsolète dans le document de sortie.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # L'objet LoadOptions possède une option pour mettre à jour tous les champs
    # marqués comme "dirty" lors du chargement du document.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # La mise à jour des champs "dirty" de cette manière définit automatiquement leur indicateur "IsDirty" sur false.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

