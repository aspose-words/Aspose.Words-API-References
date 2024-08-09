---
title: FillType enumeration
linktitle: FillType enumeration
articleTitle: FillType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.drawing.FillType enumeration. Specifies fill type for a fillable object."
type: docs
weight: 90
url: /python-net/aspose.words.drawing/filltype/
---

## FillType enumeration

Specifies fill type for a fillable object.


### Members

| Name | Description |
| --- | --- |
| SOLID | Solid fill. |
| PATTERNED | Patterned fill. |
| GRADIENT | Gradient fill. |
| TEXTURED | Textured fill. |
| BACKGROUND | Fill is the same as the background. |
| PICTURE | Picture fill. |

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

* module [aspose.words.drawing](../)

