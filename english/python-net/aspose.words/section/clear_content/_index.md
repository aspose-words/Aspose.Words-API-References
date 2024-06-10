---
title: Section.clear_content method
linktitle: clear_content method
articleTitle: clear_content method
second_title: Aspose.Words for Python
description: "Section.clear_content method. Clears the section."
type: docs
weight: 90
url: /python-net/aspose.words/section/clear_content/
---

## clear_content() {#default}

Clears the section.


```python
def clear_content(self):
    ...
```

### Remarks

The text of [Section.body](../body/) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.




### Examples

Shows how to clear the contents of a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.write('Hello world!')
self.assertEqual('Hello world!', doc.get_text().strip())
self.assertEqual(1, doc.first_section.body.paragraphs.count)
# Running the "ClearContent" method will remove all the section contents
# but leave a blank paragraph to add content again.
doc.first_section.clear_content()
self.assertEqual('', doc.get_text().strip())
self.assertEqual(1, doc.first_section.body.paragraphs.count)
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

