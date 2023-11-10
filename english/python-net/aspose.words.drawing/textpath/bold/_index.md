---
title: TextPath.bold property
linktitle: bold property
articleTitle: bold property
second_title: Aspose.Words for Python
description: "TextPath.bold property. True if the font is formatted as bold."
type: docs
weight: 10
url: /python-net/aspose.words.drawing/textpath/bold/
---

## TextPath.bold property

True if the font is formatted as bold.


```python
@property
def bold(self) -> bool:
    ...

@bold.setter
def bold(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to work with WordArt.

```python
def test_insert_text_paths(self):

    doc = aw.Document()

    # Insert a WordArt object to display text in a shape that we can re-size and move by using the mouse in Microsoft Word.
    # Provide a "ShapeType" as an argument to set a shape for the WordArt.
    shape = self.append_word_art(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, drawing.Color.white, drawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)

    # Apply the "bold" and "italic" formatting settings to the text using the respective properties.
    shape.text_path.bold = True
    shape.text_path.italic = True

    # Below are various other text formatting-related properties.
    self.assertFalse(shape.text_path.underline)
    self.assertFalse(shape.text_path.shadow)
    self.assertFalse(shape.text_path.strike_through)
    self.assertFalse(shape.text_path.reverse_rows)
    self.assertFalse(shape.text_path.x_scale)
    self.assertFalse(shape.text_path.trim)
    self.assertFalse(shape.text_path.small_caps)

    self.assertEqual(36.0, shape.text_path.size)
    self.assertEqual("Hello World! This text is bold, and italic.", shape.text_path.text)
    self.assertEqual(aw.drawing.ShapeType.TEXT_PLAIN_TEXT, shape.shape_type)

    # Use the "on" property to show/hide the text.
    shape = self.append_word_art(doc, "On set to \"True\"", "Calibri", 150, 24, drawing.Color.yellow, drawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    shape.text_path.on = True

    shape = self.append_word_art(doc, "On set to \"False\"", "Calibri", 150, 24, drawing.Color.yellow, drawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    shape.text_path.on = False

    # Use the "kerning" property to enable/disable kerning spacing between certain characters.
    shape = self.append_word_art(doc, "Kerning: VAV", "Times New Roman", 90, 24, drawing.Color.orange, drawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    shape.text_path.kerning = True

    shape = self.append_word_art(doc, "No kerning: VAV", "Times New Roman", 100, 24, drawing.Color.orange, drawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    shape.text_path.kerning = False

    # Use the "spacing" property to set the custom spacing between characters on a scale from 0.0 (none) to 1.0 (default).
    shape = self.append_word_art(doc, "Spacing set to 0.1", "Calibri", 120, 24, drawing.Color.blue_violet, drawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
    shape.text_path.spacing = 0.1

    # Set the "rotate_letters" property to "True" to rotate each character 90 degrees counterclockwise.
    shape = self.append_word_art(doc, "RotateLetters", "Calibri", 200, 36, drawing.Color.green_yellow, drawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
    shape.text_path.rotate_letters = True

    # Set the "same_letter_heights" property to "True" to get the x-height of each character to equal the cap height.
    shape = self.append_word_art(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, drawing.Color.deep_sky_blue, drawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
    shape.text_path.same_letter_heights = True

    # By default, the text's size will always scale to fit the containing shape's size, overriding the text size setting.
    shape = self.append_word_art(doc, "FitShape on", "Calibri", 160, 24, drawing.Color.light_blue, drawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    self.assertTrue(shape.text_path.fit_shape)
    shape.text_path.size = 24.0

    # If we set the "fit_shape: property to "False", the text will keep the size
    # which the "size" property specifies regardless of the size of the shape.
    # Use the "text_path_alignment" property also to align the text to a side of the shape.
    shape = self.append_word_art(doc, "FitShape off", "Calibri", 160, 24, drawing.Color.light_blue, drawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
    shape.text_path.fit_shape = False
    shape.text_path.size = 24.0
    shape.text_path.text_path_alignment = aw.drawing.TextPathAlignment.RIGHT

    doc.save(ARTIFACTS_DIR + "Shape.insert_text_paths.docx")

def append_word_art(self, doc: aw.Document, text: str, text_font_family: str, shape_width: float, shape_height: float, word_art_fill: drawing.Color, line: drawing.Color, word_art_shape_type: aw.drawing.ShapeType) -> aw.drawing.Shape:
    """Insert a new paragraph with a WordArt shape inside it."""

    # Create an inline Shape, which will serve as a container for our WordArt.
    # The shape can only be a valid WordArt shape if we assign a WordArt-designated ShapeType to it.
    # These types will have "WordArt object" in the description,
    # and their enumerator constant names will all start with "text".
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

