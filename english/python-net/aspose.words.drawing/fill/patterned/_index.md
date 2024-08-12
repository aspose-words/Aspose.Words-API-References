---
title: Fill.patterned method
linktitle: patterned method
articleTitle: patterned method
second_title: Aspose.Words for Python
description: "aspose.words.drawing.Fill.patterned method"
type: docs
weight: 230
url: /python-net/aspose.words.drawing/fill/patterned/
---

## patterned(pattern_type) {#patterntype}

Sets the specified fill to a pattern.


```python
def patterned(self, pattern_type: aspose.words.drawing.PatternType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern_type | [PatternType](../../patterntype/) | [PatternType](../../patterntype/) |

## patterned(pattern_type, fore_color, back_color) {#patterntype_color_color}

Sets the specified fill to a pattern.


```python
def patterned(self, pattern_type: aspose.words.drawing.PatternType, fore_color: aspose.pydrawing.Color, back_color: aspose.pydrawing.Color):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern_type | [PatternType](../../patterntype/) | [PatternType](../../patterntype/) |
| fore_color | aspose.pydrawing.Color | The color of the foreground fill. |
| back_color | aspose.pydrawing.Color | The color of the background fill. |

## Examples

Shows how to set pattern for a shape.

```python
doc = aw.Document(file_name=MY_DIR + 'Shape stroke pattern border.docx')
shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
fill = shape.fill
print('Pattern value is: {0}'.format(fill.pattern))
# There are several ways specified fill to a pattern.
# 1 -  Apply pattern to the shape fill:
fill.patterned(pattern_type=aw.drawing.PatternType.DIAGONAL_BRICK)
# 2 -  Apply pattern with foreground and background colors to the shape fill:
fill.patterned(pattern_type=aw.drawing.PatternType.DIAGONAL_BRICK, fore_color=aspose.pydrawing.Color.aqua, back_color=aspose.pydrawing.Color.bisque)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.FillPattern.docx')
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

