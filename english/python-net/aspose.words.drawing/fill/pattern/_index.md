---
title: Fill.pattern property
linktitle: pattern property
articleTitle: pattern property
second_title: Aspose.Words for Python
description: "Fill.pattern property. Gets a [PatternType](../../patterntype/) for the fill."
type: docs
weight: 160
url: /python-net/aspose.words.drawing/fill/pattern/
---

## Fill.pattern property

Gets a [PatternType](../../patterntype/) for the fill.



```python
@property
def pattern(self) -> aspose.words.drawing.PatternType:
    ...

```

### Examples

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

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

