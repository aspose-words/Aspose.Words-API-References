---
title: FindReplaceOptions.ignore_deleted property
linktitle: ignore_deleted property
articleTitle: ignore_deleted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_deleted property. Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /sv/python-net/aspose.words.replacing/findreplaceoptions/ignore_deleted/
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
# Börja spåra revisioner och ta bort det andra stycket, vilket kommer att skapa en raderingsrevision.
# Det stycket kommer att finnas kvar i dokumentet tills vi accepterar raderingsrevisionen.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
doc.first_section.body.paragraphs[1].remove()
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_delete_revision)
# Vi kan använda ett "FindReplaceOptions"‑objekt för att modifiera sök‑och‑ersätt‑processen.
options = aw.replacing.FindReplaceOptions()
# Ställ in flaggan "IgnoreDeleted" till "true" för att få sök‑och‑ersätt
# operationen för att ignorera stycken som är raderingsrevisioner.
# Ställ in flaggan "IgnoreDeleted" till "false" för att få sök‑och‑ersätt
# operationen för att även söka efter text i raderingsrevisioner.
options.ignore_deleted = ignore_text_inside_delete_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_delete_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

