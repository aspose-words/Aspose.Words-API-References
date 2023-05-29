---
title: FindReplaceOptions.ignore_inserted property
linktitle: ignore_inserted property
articleTitle: ignore_inserted property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_inserted property. Gets or sets a boolean value indicating either to ignore text inside insert revisions"
type: docs
weight: 100
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_inserted/
---

## FindReplaceOptions.ignore_inserted property

Gets or sets a boolean value indicating either to ignore text inside insert revisions.
The default value is ``False``.



### Examples

Shows how to include or ignore text inside insert revisions during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

# Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
doc.start_track_revisions("John Doe", datetime.now())
builder.writeln("Hello again!")
doc.stop_track_revisions()

self.assertTrue(doc.first_section.body.paragraphs[1].is_insert_revision)

# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()

# Set the "ignore_inserted" flag to "True" to get the find-and-replace
# operation to ignore paragraphs that are insert revisions.
# Set the "ignore_inserted" flag to "False" to get the find-and-replace
# operation to also search for text inside insert revisions.
options.ignore_inserted = ignore_text_inside_insert_revisions

doc.range.replace("Hello", "Greetings", options)

self.assertEqual(
    "Greetings world!\rHello again!" if ignore_text_inside_insert_revisions else "Greetings world!\rGreetings again!",
    doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

