---
title: FindReplaceOptions.ignore_deleted property
linktitle: ignore_deleted property
articleTitle: ignore_deleted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_deleted property. Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /ar/python-net/aspose.words.replacing/findreplaceoptions/ignore_deleted/
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
# ابدأ تتبع المراجعات وأزل الفقرة الثانية، مما سيخلق مراجعة حذف.
# ستستمر تلك الفقرة في المستند حتى نقبل مراجعة الحذف.
doc.start_track_revisions(author='John Doe', date_time=datetime.datetime.now())
doc.first_section.body.paragraphs[1].remove()
doc.stop_track_revisions()
self.assertTrue(doc.first_section.body.paragraphs[1].is_delete_revision)
# يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
options = aw.replacing.FindReplaceOptions()
# اضبط علامة "IgnoreDeleted" إلى "true" للحصول على عملية البحث والاستبدال
# لتجاهل الفقرات التي هي مراجعات حذف.
# اضبط علامة "IgnoreDeleted" إلى "false" للحصول على عملية البحث والاستبدال
# للبحث أيضًا عن النص داخل مراجعات الحذف.
options.ignore_deleted = ignore_text_inside_delete_revisions
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\rHello again!' if ignore_text_inside_delete_revisions else 'Greetings world!\rGreetings again!', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

