---
title: include_textboxes_footnotes_endnotes_in_stat property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether to include textboxes, footnotes and endnotes in word count statistics."
type: docs
weight: 220
url: /python-net/aspose.words/document/include_textboxes_footnotes_endnotes_in_stat/
---

## Document.include_textboxes_footnotes_endnotes_in_stat property

Specifies whether to include textboxes, footnotes and endnotes in word count statistics.


### Examples

Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("Lorem ipsum")
builder.insert_footnote(aw.notes.FootnoteType.FOOTNOTE, "sit amet")

# By default option is set to 'false'.
doc.update_word_count()

# Words count without textboxes, footnotes and endnotes.
self.assertEqual(2, doc.built_in_document_properties.words)

# Words count with textboxes, footnotes and endnotes.
doc.include_textboxes_footnotes_endnotes_in_stat = True
doc.update_word_count()

self.assertEqual(4, doc.built_in_document_properties.words)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

