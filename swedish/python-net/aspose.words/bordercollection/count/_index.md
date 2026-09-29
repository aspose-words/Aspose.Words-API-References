---
title: BorderCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "BorderCollection.count property. Gets the number of borders in the collection."
type: docs
weight: 40
url: /sv/python-net/aspose.words/bordercollection/count/
---

## BorderCollection.count property

Gets the number of borders in the collection.


```python
@property
def count(self) -> int:
    ...

```

### Examples

Shows how border collections can share elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.write('Paragraph 2.')
# Eftersom vi använde samma kantkonfiguration när vi skapade
# dessa stycken, delar deras kantsamlingar samma element.
first_paragraph_borders = doc.first_section.body.first_paragraph.paragraph_format.borders
second_paragraph_borders = builder.current_paragraph.paragraph_format.borders
i = 0
while i < first_paragraph_borders.count:
    self.assertTrue(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    self.assertFalse(first_paragraph_borders[i].is_visible)
    i += 1
for border in second_paragraph_borders:
    border.line_style = aw.LineStyle.DOT_DASH
# Efter att ha ändrat linjestilen på kanterna i endast det andra stycket,
# delar kantsamlingarna inte längre samma element.
i = 0
while i < first_paragraph_borders.count:
    self.assertFalse(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertNotEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    # Att ändra utseendet på en tom kant gör den synlig.
    self.assertTrue(second_paragraph_borders[i].is_visible)
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Border.SharedElements.docx')
```

### See Also

* module [aspose.words](../../)
* class [BorderCollection](../)

