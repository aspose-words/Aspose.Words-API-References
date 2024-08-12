---
title: Font.fill property
linktitle: fill property
articleTitle: fill property
second_title: Aspose.Words for Python
description: "Font.fill property. Gets fill formatting for the [Font](../)."
type: docs
weight: 130
url: /python-net/aspose.words/font/fill/
---

## Font.fill property

Gets fill formatting for the [Font](../).



```python
@property
def fill(self) -> aspose.words.drawing.Fill:
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

* module [aspose.words](../../)
* class [Font](../)

