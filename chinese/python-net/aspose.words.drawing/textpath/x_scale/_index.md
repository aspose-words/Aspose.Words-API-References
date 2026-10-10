---
title: TextPath.x_scale property
linktitle: x_scale property
articleTitle: x_scale property
second_title: Aspose.Words for Python
description: "TextPath.x_scale property. Determines whether a straight textpath will be used instead of the shape path."
type: docs
weight: 200
url: /zh/python-net/aspose.words.drawing/textpath/x_scale/
---

## TextPath.x_scale property

Determines whether a straight textpath will be used instead of the shape path.


```python
@property
def x_scale(self) -> bool:
    ...

@x_scale.setter
def x_scale(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.

If ``True``, the text runs along a path from left to right along the x value of 
the lower boundary of the shape.




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# 在 Microsoft Word 中插入 WordArt 对象，以在形状中显示文本，我们可以使用鼠标重新调整大小并移动。
# 提供一个 "ShapeType" 作为参数，以为 WordArt 设置形状。
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# 使用相应的属性将 "Bold" 和 "Italic" 格式设置应用于文本。
shape.text_path.bold = True
shape.text_path.italic = True
# 以下是其他各种与文本格式相关的属性。
self.assertFalse(shape.text_path.underline)
self.assertFalse(shape.text_path.shadow)
self.assertFalse(shape.text_path.strike_through)
self.assertFalse(shape.text_path.reverse_rows)
self.assertFalse(shape.text_path.x_scale)
self.assertFalse(shape.text_path.trim)
self.assertFalse(shape.text_path.small_caps)
self.assertEqual(36, shape.text_path.size)
self.assertEqual('Hello World! This text is bold, and italic.', shape.text_path.text)
self.assertEqual(aw.drawing.ShapeType.TEXT_PLAIN_TEXT, shape.shape_type)
# 使用 "On" 属性来显示/隐藏文本。
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# 使用 "Kerning" 属性来启用/禁用某些字符之间的字距调整。
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# 使用 "Spacing" 属性在 0.0（无）到 1.0（默认）的范围内设置字符之间的自定义间距。
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# 将 "RotateLetters" 属性设置为 "true"，以将每个字符逆时针旋转 90 度。
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# 将 "SameLetterHeights" 属性设置为 "true"，以使每个字符的 x 高度等于大写字母高度。
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# 默认情况下，文本大小将始终缩放以适应包含形状的大小，覆盖文本大小设置。
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# 如果我们将 "FitShape: property" 设置为 "false"，文本将保持大小
# 无论形状大小如何，均由 "Size" 属性指定。
# 还可以使用 "TextPathAlignment" 属性将文本对齐到形状的一侧。
shape = ExShape._append_word_art(doc, 'FitShape off', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.fit_shape = False
shape.text_path.size = 24
shape.text_path.text_path_alignment = aw.drawing.TextPathAlignment.RIGHT
doc.save(file_name=ARTIFACTS_DIR + 'Shape.InsertTextPaths.docx')
```

Shows how to work with WordArt (AppendWordArt).

```python
@staticmethod
def _append_word_art(doc, text, text_font_family, shape_width, shape_height, word_art_fill, line, word_art_shape_type):
    # 创建一个内联 Shape，它将作为我们 WordArt 的容器。
    # 只有在我们为其分配 WordArt 指定的 ShapeType 时，该形状才是有效的 WordArt 形状。
    # 这些类型的描述中将包含 "WordArt object"，
    # 并且它们的枚举常量名称都将以 "Text" 开头。
    shape = aw.drawing.Shape(doc, word_art_shape_type)
    shape.wrap_type = aw.drawing.WrapType.INLINE
    shape.width = shape_width
    shape.height = shape_height
    shape.fill_color = word_art_fill
    shape.stroke_color = line
    shape.text_path.text = text
    shape.text_path.font_family = text_font_family
    para = doc.first_section.body.append_child(aw.Paragraph(doc)).as_paragraph()
    para.append_child(shape)
    return shape
```

### See Also

* module [aspose.words.drawing](../../)
* class [TextPath](../)

