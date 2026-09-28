---
title: FindReplaceOptions.ignore_deleted property
linktitle: ignore_deleted property
articleTitle: ignore_deleted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_deleted property. Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /de/python-net/aspose.words.replacing/findreplaceoptions/ignore_deleted/
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
# Beginnen Sie, Revisionen zu verfolgen und entfernen Sie den zweiten Absatz, wodurch eine Löschrevision erstellt wird.
# Dieser Absatz bleibt im Dokument, bis wir die Löschrevision akzeptieren.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
doc.first_section.body.paragraphs[1].remove()
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_delete_revision)
# Wir können ein "FindReplaceOptions"‑Objekt verwenden, um den Suchen‑und‑Ersetzen‑Vorgang zu ändern.
options = aw.replacing.FindReplaceOptions()
# Setzen Sie das Flag "IgnoreDeleted" auf "true", um die Suchen‑und‑Ersetzen‑Operation zu erhalten
# Operation, um Absätze zu ignorieren, die Löschrevisionen sind.
# Setzen Sie das Flag "IgnoreDeleted" auf "false", um die Suchen‑und‑Ersetzen‑Operation zu erhalten
# Operation, um zusätzlich nach Text innerhalb von Löschrevisionen zu suchen.
options.ignore_deleted = ignore_text_inside_delete_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_delete_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

