---
title: TextBox.vertical_anchor property
linktitle: vertical_anchor property
articleTitle: vertical_anchor property
second_title: Aspose.Words for Python
description: "TextBox.vertical_anchor property. Specifies the vertical alignment of the text within a shape."
type: docs
weight: 120
url: /sv/python-net/aspose.words.drawing/textbox/vertical_anchor/
---

## TextBox.vertical_anchor property

Specifies the vertical alignment of the text within a shape.


```python
@property
def vertical_anchor(self) -> aspose.words.drawing.TextBoxAnchor:
    ...

@vertical_anchor.setter
def vertical_anchor(self, value: aspose.words.drawing.TextBoxAnchor):
    ...

```

### Remarks

The default value is [TextBoxAnchor.TOP](../../textboxanchor/#TOP).




### Examples

Shows how to vertically align the text contents of a text box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
shape = builder.insert_shape(shape_type=aw.drawing.ShapeType.TEXT_BOX, width=200, height=200)
# Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" för att
# justera texten i den här textrutan med den övre sidan av formen.
# Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" för att
# justera texten i den här textrutan till mitten av formen.
# Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" för att
# justera texten i den här textrutan till botten av formen.
shape.text_box.vertical_anchor = vertical_anchor
builder.move_to(shape.first_paragraph)
builder.write('Hello world!')
# Den vertikala justeringen av text i textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc.compatibility_options.optimize_for(aw.settings.MsWordVersion.WORD2007)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.VerticalAnchor.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextBox](../)

