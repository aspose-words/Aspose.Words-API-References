---
title: PatternType enumeration
linktitle: PatternType enumeration
articleTitle: PatternType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.PatternType enumeration. Specifies the fill pattern to be used to fill a shape."
type: docs
weight: 270
url: /python-net/aspose.words.drawing/patterntype/
---

## PatternType enumeration

Specifies the fill pattern to be used to fill a shape.


### Members

| Name | Description |
| --- | --- |
| NONE | No pattern. |
| PERCENT10 | 10% of the foreground color. |
| PERCENT20 | 20% of the foreground color. |
| PERCENT25 | 25% of the foreground color. |
| PERCENT30 | 30% of the foreground color. |
| PERCENT40 | 40% of the foreground color |
| PERCENT50 | 50% of the foreground color |
| PERCENT5 | 5% of the foreground color. |
| PERCENT60 | 60% of the foreground color. |
| PERCENT70 | 70% of the foreground color. |
| PERCENT75 | 75% of the foreground color. |
| PERCENT80 | 80% of the foreground color. |
| PERCENT90 | 90% of the foreground color. |
| CROSS | Cross. |
| DARK_DOWNWARD_DIAGONAL | Dark downward diagonal. |
| DARK_HORIZONTAL | Dark horizontal. |
| DARK_UPWARD_DIAGONAL | Dark upward diagonal. |
| DARK_VERTICAL | Dark vertical. |
| DASHED_DOWNWARD_DIAGONAL | Dashed downward diagonal. |
| DASHED_HORIZONTAL | Dashed horizontal. |
| DASHED_UPWARD_DIAGONAL | Dashed upward diagonal. |
| DASHED_VERTICAL | Dashed vertical. |
| DIAGONAL_BRICK | Diagonal brick. |
| DIAGONAL_CROSS | Diagonal cross. |
| DIVOT | Pattern divot. |
| DOTTED_DIAMOND | Dotted diamond. |
| DOTTED_GRID | Dotted grid. |
| DOWNWARD_DIAGONAL | Downward diagonal. |
| HORIZONTAL | Horizontal. |
| HORIZONTAL_BRICK | Horizontal brick. |
| LARGE_CHECKER_BOARD | Large checker board. |
| LARGE_CONFETTI | Large confetti. |
| LARGE_GRID | Large grid. |
| LIGHT_DOWNWARD_DIAGONAL | Light downward diagonal. |
| LIGHT_HORIZONTAL | Light horizontal. |
| LIGHT_UPWARD_DIAGONAL | Light upward diagonal. |
| LIGHT_VERTICAL | Light vertical. |
| NARROW_HORIZONTAL | Narrow horizontal. |
| NARROW_VERTICAL | Narrow vertical. |
| OUTLINED_DIAMOND | Outlined diamond. |
| PLAID | Plaid. |
| SHINGLE | Shingle. |
| SMALL_CHECKER_BOARD | Small checker board. |
| SMALL_CONFETTI | Small confetti. |
| SMALL_GRID | Small grid. |
| SOLID_DIAMOND | Solid diamond. |
| SPHERE | Sphere. |
| TRELLIS | Trellis. |
| UPWARD_DIAGONAL | Upward diagonal. |
| VERTICAL | Vertical. |
| WAVE | Wave. |
| WEAVE | Weave. |
| WIDE_DOWNWARD_DIAGONAL | Wide downward diagonal. |
| WIDE_UPWARD_DIAGONAL | Wide upward diagonal. |
| ZIG_ZAG | Zig zag. |

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

* module [aspose.words.drawing](../)

