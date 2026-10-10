---
title: SaveOptions.update_fields property
linktitle: update_fields property
articleTitle: update_fields property
second_title: Aspose.Words for Python
description: "SaveOptions.update_fields property. Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format"
type: docs
weight: 150
url: /it/python-net/aspose.words.saving/saveoptions/update_fields/
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
# Inserisci testo con i campi PAGE e NUMPAGES. Questi campi non mostrano il valore corretto in tempo reale.
# Dovremo aggiornarli manualmente usando metodi di aggiornamento come "Field.Update()" e "Document.UpdateFields()"
# ogni volta che dobbiamo farli visualizzare valori accurati.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' of ')
builder.insert_field(field_code='NUMPAGES', field_value='')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Hello World!')
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Imposta la proprietà "UpdateFields" su "false" per non aggiornare tutti i campi in un documento subito prima di un'operazione di salvataggio.
# Questa è l'opzione preferibile se sappiamo che tutti i nostri campi saranno aggiornati prima del salvataggio.
# Imposta la proprietà "UpdateFields" su "true" per iterare attraverso tutto il documento
# i campi e aggiornarli prima di salvarlo come PDF. Questo garantirà che tutti i campi vengano visualizzati
# con i valori più accurati nel PDF.
options.update_fields = update_fields
# Possiamo clonare gli oggetti PdfSaveOptions.
self.assertNotEqual(options, options.clone())
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.UpdateFields.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

