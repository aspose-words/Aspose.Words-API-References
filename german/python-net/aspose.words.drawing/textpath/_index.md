---
title: TextPath class
linktitle: TextPath class
articleTitle: TextPath class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextPath class. Defines the text and formatting of the text path (of a WordArt object)"
type: docs
weight: 480
url: /de/python-net/aspose.words.drawing/textpath/
---

## TextPath class

Defines the text and formatting of the text path (of a WordArt object).
To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/python-net/working-with-shapes/) documentation article.




### Remarks

Use the [Shape.text_path](../shape/text_path/) property to access WordArt properties of a shape.
You do not create instances of the [TextPath](./) class directly.




### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | True if the font is formatted as bold. |
| [fit_path](./fit_path/) | Defines whether the text fits the path of a shape. |
| [fit_shape](./fit_shape/) | Defines whether the text fits bounding box of a shape. |
| [font_family](./font_family/) | Defines the family of the textpath font. |
| [italic](./italic/) | True if the font is formatted as italic. |
| [kerning](./kerning/) | Determines whether kerning is turned on. |
| [on](./on/) | Defines whether the text is displayed. |
| [reverse_rows](./reverse_rows/) | Determines whether the layout order of rows is reversed. |
| [rotate_letters](./rotate_letters/) | Determines whether the letters of the text are rotated. |
| [same_letter_heights](./same_letter_heights/) | Determines whether all letters will be the same height regardless of initial case. |
| [shadow](./shadow/) | Defines whether a shadow is applied to the text on a text path. |
| [size](./size/) | Defines the size of the font in points. |
| [small_caps](./small_caps/) | True if the font is formatted as small capital letters. |
| [spacing](./spacing/) | Defines the amount of spacing for text. 1 means 100%. |
| [strike_through](./strike_through/) | True if the font is formatted as strikethrough text. |
| [text](./text/) | Defines the text of the text path. |
| [text_path_alignment](./text_path_alignment/) | Defines the alignment of text. |
| [trim](./trim/) | Determines whether extra space is removed above and below the text. |
| [underline](./underline/) | True if the font is underlined. |
| [x_scale](./x_scale/) | Determines whether a straight textpath will be used instead of the shape path. |

### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# Fügen Sie ein WordArt-Objekt ein, um Text in einer Form anzuzeigen, die wir mit der Maus in Microsoft Word skalieren und verschieben können.
# Geben Sie einen "ShapeType" als Argument an, um eine Form für das WordArt festzulegen.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Wenden Sie die Formatierungseinstellungen "Bold" und "Italic" auf den Text an, indem Sie die jeweiligen Eigenschaften verwenden.
shape.text_path.bold = True
shape.text_path.italic = True
# Im Folgenden finden Sie verschiedene weitere textformatierungsbezogene Eigenschaften.
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
# Verwenden Sie die Eigenschaft "On", um den Text ein- bzw. auszublenden.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Verwenden Sie die Eigenschaft "Kerning", um den Kerning-Abstand zwischen bestimmten Zeichen zu aktivieren/deaktivieren.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# Verwenden Sie die Eigenschaft "Spacing", um den benutzerdefinierten Abstand zwischen Zeichen auf einer Skala von 0,0 (keine) bis 1,0 (Standard) festzulegen.
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# Setzen Sie die Eigenschaft "RotateLetters" auf "true", um jedes Zeichen um 90 Grad gegen den Uhrzeigersinn zu drehen.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# Setzen Sie die Eigenschaft "SameLetterHeights" auf "true", um die x-Höhe jedes Zeichens gleich der Kapitälchenhöhe zu erhalten.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# Standardmäßig wird die Textgröße immer so skaliert, dass sie in die Größe der enthaltenden Form passt, wodurch die Einstellung der Textgröße überschrieben wird.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Wenn wir die Eigenschaft "FitShape" auf "false" setzen, behält der Text die Größe bei
# die durch die Eigenschaft "Size" festgelegt wird, unabhängig von der Größe der Form.
# Verwenden Sie die Eigenschaft "TextPathAlignment" ebenfalls, um den Text an einer Seite der Form auszurichten.
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
    # Erstellen Sie eine Inline-Shape, die als Container für unser WordArt dient.
    # Die Form kann nur eine gültige WordArt-Form sein, wenn wir ihr einen für WordArt vorgesehenen ShapeType zuweisen.
    # Diese Typen werden in der Beschreibung "WordArt object" enthalten,
    # und ihre Aufzählungskonstantennamen beginnen alle mit "Text".
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

* module [aspose.words.drawing](../)
* property [Shape.text_path](../shape/text_path/)

