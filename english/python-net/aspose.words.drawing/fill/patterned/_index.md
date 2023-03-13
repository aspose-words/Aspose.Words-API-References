---
title: patterned method
second_title: Aspose.Words for Python via .NET API Reference
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
| pattern_type | [PatternType](../../patterntype/) |  |

## patterned(pattern_type, fore_color, back_color) {#patterntype_color_color}

Sets the specified fill to a pattern.


```python
def patterned(self, pattern_type: aspose.words.drawing.PatternType, fore_color: aspose.pydrawing.Color, back_color: aspose.pydrawing.Color):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pattern_type | [PatternType](../../patterntype/) |  |
| fore_color | aspose.pydrawing.Color |  |
| back_color | aspose.pydrawing.Color |  |

## Examples

Shows how to set pattern for a shape.

```python
doc = aw.Document(MY_DIR + "Shape stroke pattern border.docx")

shape = doc.get_child(aw.NodeType.SHAPE, 0, True).as_shape()
fill = shape.fill

print("Pattern value is:", fill.pattern)

# There are several ways specified fill to a pattern.
# 1 -  Apply pattern to the shape fill:
fill.patterned(aw.drawing.PatternType.DIAGONAL_BRICK)

# 2 -  Apply pattern with foreground and background colors to the shape fill:
fill.patterned(aw.drawing.PatternType.DIAGONAL_BRICK, drawing.Color.aqua, drawing.Color.bisque)

doc.save(ARTIFACTS_DIR + "Shape.fill_pattern.docx")
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

