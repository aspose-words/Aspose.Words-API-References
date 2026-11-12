---
title: FindReplaceOptions.ignore_inserted property
linktitle: ignore_inserted property
articleTitle: ignore_inserted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_inserted property. Gets or sets a boolean value indicating either to ignore text inside insert revisions"
type: docs
weight: 100
url: /ru/python-net/aspose.words.replacing/findreplaceoptions/ignore_inserted/
---

## FindReplaceOptions.ignore_inserted property

Gets or sets a boolean value indicating either to ignore text inside insert revisions.
The default value is ``False``.



```python
@property
def ignore_inserted(self) -> bool:
    ...

@ignore_inserted.setter
def ignore_inserted(self, value: bool):
    ...

```

### Examples

Shows how to include or ignore text inside insert revisions during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Начните отслеживание изменений и вставьте абзац. Этот абзац будет вставкой‑изменением.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
builder.writeln('Hello again!')
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_insert_revision)
# Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
options = aw.replacing.FindReplaceOptions()
# Установите флаг "IgnoreInserted" в значение "true", чтобы операция поиска и замены
# игнорировала абзацы, являющиеся вставками‑изменениями.
# Установите флаг "IgnoreInserted" в значение "false", чтобы операция поиска и замены
# также искала текст внутри вставок‑изменений.
options.ignore_inserted = ignore_text_inside_insert_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_insert_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

