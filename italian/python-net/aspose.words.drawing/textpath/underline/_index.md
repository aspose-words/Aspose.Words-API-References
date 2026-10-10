---
title: TextPath.underline property
linktitle: underline property
articleTitle: underline property
second_title: Aspose.Words for Python
description: "TextPath.underline property. True if the font is underlined."
type: docs
weight: 190
url: /it/python-net/aspose.words.drawing/textpath/underline/
---

## TextPath.underline property

True if the font is underlined.


```python
@property
def underline(self) -> bool:
    ...

@underline.setter
def underline(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# Inserisci un oggetto WordArt per visualizzare il testo in una forma che possiamo ridimensionare e spostare usando il mouse in Microsoft Word.
# Fornisci un "ShapeType" come argomento per impostare una forma per il WordArt.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Applica le impostazioni di formattazione "Bold" e "Italic" al testo usando le rispettive proprietà.
shape.text_path.bold = True
shape.text_path.italic = True
# Di seguito sono riportate varie altre proprietà relative alla formattazione del testo.
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
# Usa la proprietà "On" per mostrare/nascondere il testo.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Usa la proprietà "Kerning" per abilitare/disabilitare la spaziatura di kerning tra alcuni caratteri.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# Usa la proprietà "Spacing" per impostare la spaziatura personalizzata tra i caratteri su una scala da 0.0 (nessuna) a 1.0 (predefinita).
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# Imposta la proprietà "RotateLetters" su "true" per ruotare ogni carattere di 90 gradi in senso antiorario.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# Imposta la proprietà "SameLetterHeights" su "true" per far sì che l'altezza x di ogni carattere sia uguale all'altezza delle maiuscole.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# Per impostazione predefinita, la dimensione del testo verrà sempre scalata per adattarsi alla dimensione della forma contenente, sovrascrivendo l'impostazione della dimensione del testo.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Se impostiamo la proprietà "FitShape" su "false", il testo manterrà la dimensione
# che la proprietà "Size" specifica indipendentemente dalla dimensione della forma.
# Usa anche la proprietà "TextPathAlignment" per allineare il testo a un lato della forma.
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
    # Crea una Shape inline, che servirà da contenitore per il nostro WordArt.
    # La forma può essere una forma WordArt valida solo se le assegniamo un ShapeType designato per WordArt.
    # Questi tipi avranno "WordArt object" nella descrizione,
    # e i loro nomi di costante enumeratore inizieranno tutti con "Text".
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

