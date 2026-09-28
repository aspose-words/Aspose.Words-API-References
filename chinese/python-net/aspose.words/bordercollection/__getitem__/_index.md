---
title: BorderCollection indexer
linktitle: BorderCollection indexer
articleTitle: BorderCollection indexer
second_title: Aspose.Words for Python
description: "BorderCollection indexer. Retrieves a [Border](../../border/) object by index."
type: docs
weight: 10
url: /zh/python-net/aspose.words/bordercollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Retrieves a [Border](../../border/) object by index.



```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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
* class [BorderCollection](../)

