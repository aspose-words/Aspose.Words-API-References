---
title: ignore_deleted property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value indicating either to ignore text inside delete revisions"
type: docs
weight: 60
url: /python-net/aspose.words.replacing/findreplaceoptions/ignore_deleted/
---

## FindReplaceOptions.ignore_deleted property

Gets or sets a boolean value indicating either to ignore text inside delete revisions.
The default value is ``False``.



### Examples

Shows how to include or ignore text inside delete revisions during a find-and-replace operation.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")
builder.writeln("Hello again!")

# Start tracking revisions and remove the second paragraph, which will create a delete revision.
# That paragraph will persist in the document until we accept the delete revision.
doc.start_track_revisions("John Doe", datetime.now())
doc.first_section.body.paragraphs[1].remove()
doc.stop_track_revisions()

self.assertTrue(doc.first_section.body.paragraphs[1].is_delete_revision)

# We can use a "FindReplaceOptions" object to modify the find and replace process.
options = aw.replacing.FindReplaceOptions()

# Set the "ignore_deleted" flag to "True" to get the find-and-replace
# operation to ignore paragraphs that are delete revisions.
# Set the "ignore_deleted" flag to "False" to get the find-and-replace
# operation to also search for text inside delete revisions.
options.ignore_deleted = ignore_text_inside_delete_revisions

doc.range.replace("Hello", "Greetings", options)

self.assertEqual(
    "Greetings world!\rHello again!" if ignore_text_inside_delete_revisions else "Greetings world!\rGreetings again!",
    doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

