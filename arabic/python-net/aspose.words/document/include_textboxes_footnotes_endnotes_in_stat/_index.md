---
title: Document.include_textboxes_footnotes_endnotes_in_stat property
linktitle: include_textboxes_footnotes_endnotes_in_stat property
articleTitle: include_textboxes_footnotes_endnotes_in_stat property
second_title: Aspose.Words for Python
description: "Document.include_textboxes_footnotes_endnotes_in_stat property. Specifies whether to include textboxes, footnotes and endnotes in word count statistics."
type: docs
weight: 230
url: /ar/python-net/aspose.words/document/include_textboxes_footnotes_endnotes_in_stat/
---

## Document.include_textboxes_footnotes_endnotes_in_stat property

Specifies whether to include textboxes, footnotes and endnotes in word count statistics.


```python
@property
def include_textboxes_footnotes_endnotes_in_stat(self) -> bool:
    ...

@include_textboxes_footnotes_endnotes_in_stat.setter
def include_textboxes_footnotes_endnotes_in_stat(self, value: bool):
    ...

```

### Examples

Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Lorem ipsum')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='sit amet')
# الخيار الافتراضي مضبوط على 'false'.
doc.update_word_count()
# عدد الكلمات بدون مربعات النص والحواشي وهوامش النهاية.
self.assertEqual(2, doc.built_in_document_properties.words)
doc.include_textboxes_footnotes_endnotes_in_stat = True
doc.update_word_count()
# عدد الكلمات مع مربعات النص والحواشي وهوامش النهاية.
self.assertEqual(4, doc.built_in_document_properties.words)
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

