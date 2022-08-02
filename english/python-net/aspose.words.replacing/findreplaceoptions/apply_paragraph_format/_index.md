---
title: apply_paragraph_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Paragraph formatting applied to new content."
type: docs
weight: 30
url: /python-net/aspose.words.replacing/findreplaceoptions/apply_paragraph_format/
---

## FindReplaceOptions.apply_paragraph_format property

Paragraph formatting applied to new content.


### Examples

Shows how to add formatting to paragraphs in which a find-and-replace operation has found matches.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.")
builder.writeln("This one will not!")
builder.write("This one also will.")

paragraphs = doc.first_section.body.paragraphs

self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[2].paragraph_format.alignment)

# We can use a "FindReplaceOptions" object to modify the find-and-replace process.
options = aw.replacing.FindReplaceOptions()

# Set the "alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
# that contains a match that the find-and-replace operation finds.
options.apply_paragraph_format.alignment = aw.ParagraphAlignment.RIGHT

# Replace every full stop that is right before a paragraph break with an exclamation point.
count = doc.range.replace(".&p", "!&p", options)

self.assertEqual(2, count)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[0].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.LEFT, paragraphs[1].paragraph_format.alignment)
self.assertEqual(aw.ParagraphAlignment.RIGHT, paragraphs[2].paragraph_format.alignment)
self.assertEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                 "This one will not!\r" +
                 "This one also will!", doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

