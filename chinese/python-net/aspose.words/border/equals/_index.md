---
title: Border.equals method
linktitle: equals method
articleTitle: equals method
second_title: Aspose.Words for Python
description: "Border.equals method. Determines whether the specified border is equal in value to the current border."
type: docs
weight: 100
url: /zh/python-net/aspose.words/border/equals/
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
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.write('Paragraph 2.')
# 由于我们在创建时使用了相同的边框配置
# 这些段落的边框集合共享相同的元素。
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
# 在仅更改第二段边框的线型后，
# 边框集合不再共享相同的元素。
i = 0
while i < first_paragraph_borders.count:
    self.assertFalse(first_paragraph_borders[i].equals(rhs=second_paragraph_borders[i]))
    self.assertNotEqual(hash(first_paragraph_borders[i]), hash(second_paragraph_borders[i]))
    # 更改空白边框的外观会使其可见。
    self.assertTrue(second_paragraph_borders[i].is_visible)
    i += 1
doc.save(file_name=ARTIFACTS_DIR + 'Border.SharedElements.docx')
```

### See Also

* module [aspose.words](../../)
* class [Border](../)

