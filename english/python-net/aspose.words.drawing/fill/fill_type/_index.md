---
title: Fill.fill_type property
linktitle: fill_type property
articleTitle: fill_type property
second_title: Aspose.Words for Python
description: "Fill.fill_type property. Gets a fill type."
type: docs
weight: 60
url: /python-net/aspose.words.drawing/fill/fill_type/
---

## Fill.fill_type property

Gets a fill type.


```python
@property
def fill_type(self) -> aspose.words.drawing.FillType:
    ...

```

### Examples

Shows how to convert any of the fills back to solid fill.

```python
doc = aw.Document(file_name=MY_DIR + 'Two color gradient.docx')
# Get Fill object for Font of the first Run.
fill = doc.first_section.body.paragraphs[0].runs[0].font.fill
# Check Fill properties of the Font.
print('The type of the fill is: {0}'.format(fill.fill_type))
print('The foreground color of the fill is: {0}'.format(fill.fore_color))
print('The fill is transparent at {0}%'.format(fill.transparency * 100))
# Change type of the fill to Solid with uniform green color.
fill.solid()
print('\nThe fill is changed:')
print('The type of the fill is: {0}'.format(fill.fill_type))
print('The foreground color of the fill is: {0}'.format(fill.fore_color))
print('The fill transparency is {0}%'.format(fill.transparency * 100))
doc.save(file_name=ARTIFACTS_DIR + 'Drawing.FillSolid.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [Fill](../)

