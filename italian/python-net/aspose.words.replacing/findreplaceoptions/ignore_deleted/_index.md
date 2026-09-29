---
title: FindReplaceOptions.ignore_deleted property
linktitle: ignore_deleted property
articleTitle: ignore_deleted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_deleted property. Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /it/python-net/aspose.words.replacing/findreplaceoptions/ignore_deleted/
---

## FindReplaceOptions.ignore_deleted property

Gets or sets a boolean value indicating either to ignore text inside delete revisions.
The default value is ``False``.



```python
@property
def ignore_deleted(self) -> bool:
    ...

@ignore_deleted.setter
def ignore_deleted(self, value: bool):
    ...

```

### Examples

Shows how to include or ignore text inside delete revisions during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.writeln('Hello again!')
# Inizia a tenere traccia delle revisioni e rimuovi il secondo paragrafo, il che creerà una revisione di eliminazione.
# Quel paragrafo persisterà nel documento finché non accetteremo la revisione di eliminazione.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
doc.first_section.body.paragraphs[1].remove()
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_delete_revision)
# Possiamo usare un oggetto "FindReplaceOptions" per modificare il processo di trova e sostituisci.
options = aw.replacing.FindReplaceOptions()
# Imposta il flag "IgnoreDeleted" su "true" per ottenere l'operazione di trova-e-sostituisci
# che ignora i paragrafi che sono revisioni di eliminazione.
# Imposta il flag "IgnoreDeleted" su "false" per ottenere l'operazione di trova-e-sostituisci
# che ricerca anche il testo all'interno delle revisioni di eliminazione.
options.ignore_deleted = ignore_text_inside_delete_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_delete_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

