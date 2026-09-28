---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /fr/python-net/aspose.words.saving/saveoptions/update_fields/
---

## SaveOptions.update_fields property

Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format.
Default value for this property is ``True``.



```python
@property
def update_fields(self) -> bool:
    ...

@update_fields.setter
def update_fields(self, value: bool):
    ...

```

### Remarks

Allows to specify whether to mimic or not MS Word behavior.


### Examples

Shows how to update all the fields in a document immediately before saving it to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Insérer du texte avec les champs PAGE et NUMPAGES. Ces champs n'affichent pas la valeur correcte en temps réel.
# Nous devrons les mettre à jour manuellement en utilisant des méthodes de mise à jour telles que "Field.Update()" et "Document.UpdateFields()"
# à chaque fois que nous avons besoin qu'ils affichent des valeurs précises.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Définissez la propriété "UpdateFields" sur "false" pour ne pas mettre à jour tous les champs d'un document juste avant une opération d'enregistrement.
# C'est l'option préférable si nous savons que tous nos champs seront à jour avant l'enregistrement.
# Définissez la propriété "UpdateFields" sur "true" pour parcourir tout le document
# les champs et les mettre à jour avant de l'enregistrer en PDF. Cela garantira que tous les champs afficheront
# les valeurs les plus précises dans le PDF.
options.update_fields = update_fields
# Nous pouvons cloner des objets PdfSaveOptions.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

