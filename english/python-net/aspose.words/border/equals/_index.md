---
title: Border.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "Border.equals method. Determines whether the specified border is equal in value to the current border."
type: docs
weight: 100
url: /python-net/aspose.words/border/equals/
---

## equals(rhs) {#border}

Determines whether the specified border is equal in value to the current border.


```python
def equals(self, rhs: aspose.words.Border):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| rhs | [Border](../) |  |

### Examples

Shows how border collections can share elements.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Paragraph 1.')
builder.write('Paragraph 2.')
# Since we used the same border configuration while creating
# these paragraphs, their border collections share the same elements.
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
# After changing the line style of the borders in just the second paragraph,
# the border collections no longer share the same elements.
i = 0
while i < first_paragraph_borders.count:
    self.assertFalse(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertNotEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    # Changing the appearance of an empty border makes it visible.
    self.assertTrue(second_paragraph_borders[i].is_visible)
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Border.SharedElements.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

