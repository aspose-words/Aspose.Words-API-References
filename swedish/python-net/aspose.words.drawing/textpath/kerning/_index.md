---
title: TextPath.kerning property
linktitle: kerning property
articleTitle: kerning property
second_title: Aspose.Words for Python
description: "TextPath.kerning property. Determines whether kerning is turned on."
type: docs
weight: 60
url: /sv/python-net/aspose.words.drawing/textpath/kerning/
---

## TextPath.kerning property

Determines whether kerning is turned on.


```python
@property
def kerning(self) -> bool:
    ...

@kerning.setter
def kerning(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# Infoga ett WordArt-objekt för att visa text i en form som vi kan ändra storlek på och flytta med musen i Microsoft Word.
# Tillhandahåll en "ShapeType" som argument för att ange en form för WordArt.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Tilldela formateringsinställningarna "Bold" och "Italic" till texten med hjälp av respektive egenskaper.
shape.text_path.bold = True
shape.text_path.italic = True
# Nedan följer olika andra egenskaper relaterade till textformatering.
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
# Använd egenskapen "On" för att visa/dölja texten.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Använd egenskapen "Kerning" för att aktivera/inaktivera kerningavstånd mellan vissa tecken.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# Använd egenskapen "Spacing" för att ange anpassat avstånd mellan tecken på en skala från 0.0 (ingen) till 1.0 (standard).
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# Ställ in egenskapen "RotateLetters" till "true" för att rotera varje tecken 90 grader moturs.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# Ställ in egenskapen "SameLetterHeights" till "true" för att få x-höjden för varje tecken att vara lika med versalhöjden.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# Som standard kommer textens storlek alltid att skalas för att passa den omgivande formens storlek, vilket åsidosätter inställningen för textstorlek.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Om vi ställer in egenskapen "FitShape" till "false" kommer texten att behålla storleken
# som egenskapen "Size" specificerar oavsett formens storlek.
# Använd egenskapen "TextPathAlignment" också för att justera texten till en sida av formen.
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
    # Skapa en inline Shape som kommer att fungera som en behållare för vår WordArt.
    # Formen kan endast vara en giltig WordArt-form om vi tilldelar den en WordArt‑designad ShapeType.
    # Dessa typer kommer att ha "WordArt object" i beskrivningen,
    # och deras uppräkningskonstantnamn kommer alla att börja med "Text".
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

