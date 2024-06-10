---
title: ParagraphFormat.character_unit_first_line_indent property
linktitle: character_unit_first_line_indent property
articleTitle: character_unit_first_line_indent property
second_title: Aspose.Words for Python
description: "ParagraphFormat.character_unit_first_line_indent property. Gets or sets the value (in characters) for the first-line or hanging indent"
type: docs
weight: 70
url: /python-net/aspose.words/paragraphformat/character_unit_first_line_indent/
---

## ParagraphFormat.character_unit_first_line_indent property

Gets or sets the value (in characters) for the first-line or hanging indent.
Use positive values to set the first-line indent, and negative values to set the hanging indent.




```python
@property
def character_unit_first_line_indent(self) -> float:
    ...

@character_unit_first_line_indent.setter
def character_unit_first_line_indent(self, value: float):
    ...

```

### Examples

Shows how to change paragraph spacing and indents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
format = doc.first_section.body.first_paragraph.paragraph_format
# Below are five different spacing options, along with the properties that their configuration indirectly affects.
# 1 -  Left indent:
self.assertEqual(format.left_indent, 0.0)
format.character_unit_left_indent = 10.0
self.assertEqual(format.left_indent, 120.0)
# 2 -  Right indent:
self.assertEqual(format.right_indent, 0.0)
format.character_unit_right_indent = -5.5
self.assertEqual(format.right_indent, -66.0)
# 3 -  Hanging indent:
self.assertEqual(format.first_line_indent, 0.0)
format.character_unit_first_line_indent = 20.3
self.assertAlmostEqual(format.first_line_indent, 243.59, delta=0.1)
# 4 -  Line spacing before paragraphs:
self.assertEqual(format.space_before, 0.0)
format.line_unit_before = 5.1
self.assertAlmostEqual(format.space_before, 61.1, delta=0.1)
# 5 -  Line spacing after paragraphs:
self.assertEqual(format.space_after, 0.0)
format.line_unit_after = 10.9
self.assertAlmostEqual(format.space_after, 130.8, delta=0.1)
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.write('测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试' + '文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

