---
title: solid method
second_title: Aspose.Words for Python via .NET API Reference
description: "aspose.words.drawing.Fill.solid method"
type: docs
weight: 260
url: /python-net/aspose.words.drawing/fill/solid/
---

## solid() {#default}

Sets the fill to a uniform color.


```python
def solid(self):
    ...
```

Use this method to convert any of the fills back to solid fill.


## solid(color) {#color}

Sets the fill to a specified uniform color.


```python
def solid(self, color: aspose.pydrawing.Color):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| color | aspose.pydrawing.Color |  |

Use this method to convert any of the fills back to solid fill.


## Examples

Shows how to convert any of the fills back to solid fill.

```python
doc = aw.Document(MY_DIR + "Two color gradient.docx")

# Get Fill object for Font of the first Run.
fill = doc.first_section.body.paragraphs[0].runs[0].font.fill

# Check "fill" properties of the Font.
print("The type of the fill is:", fill.fill_type)
print("The foreground color of the fill is:", fill.fore_color)
print("The fill is transparent at", fill.transparency * 100, "%")

# Change type of the fill to Solid with uniform green color.
fill.solid(drawing.Color.green)
print("\nThe fill is changed:")
print("The type of the fill is:", fill.fill_type)
print("The foreground color of the fill is:", fill.fore_color)
print("The fill transparency is", fill.transparency * 100, "%")

doc.save(ARTIFACTS_DIR + "Drawing.fill_solid.docx")
```

## See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

