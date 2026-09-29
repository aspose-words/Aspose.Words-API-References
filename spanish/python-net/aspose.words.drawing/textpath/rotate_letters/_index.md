---
title: TextPath.rotate_letters property
linktitle: rotate_letters property
articleTitle: rotate_letters property
second_title: Aspose.Words for Python
description: "TextPath.rotate_letters property. Determines whether the letters of the text are rotated."
type: docs
weight: 90
url: /es/python-net/aspose.words.drawing/textpath/rotate_letters/
---

## TextPath.rotate_letters property

Determines whether the letters of the text are rotated.


```python
@property
def rotate_letters(self) -> bool:
    ...

@rotate_letters.setter
def rotate_letters(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# Inserte un objeto WordArt para mostrar texto en una forma que podamos redimensionar y mover usando el mouse en Microsoft Word.
# Proporcione un "ShapeType" como argumento para establecer una forma para el WordArt.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Aplique los ajustes de formato "Bold" y "Italic" al texto usando las propiedades correspondientes.
shape.text_path.bold = True
shape.text_path.italic = True
# A continuación se presentan varias propiedades relacionadas con el formato de texto.
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
# Utilice la propiedad "On" para mostrar/ocultar el texto.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Utilice la propiedad "Kerning" para habilitar/deshabilitar el espaciado de kerning entre ciertos caracteres.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# Utilice la propiedad "Spacing" para establecer el espaciado personalizado entre caracteres en una escala de 0.0 (ninguno) a 1.0 (predeterminado).
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# Establezca la propiedad "RotateLetters" en "true" para rotar cada carácter 90 grados en sentido antihorario.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# Establezca la propiedad "SameLetterHeights" en "true" para que la altura x de cada carácter sea igual a la altura de mayúsculas.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# Por defecto, el tamaño del texto siempre se escalará para ajustarse al tamaño de la forma contenedora, sobrescribiendo la configuración del tamaño del texto.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Si establecemos la propiedad "FitShape" en "false", el texto mantendrá el tamaño
# que la propiedad "Size" especifica, sin importar el tamaño de la forma.
# Utilice también la propiedad "TextPathAlignment" para alinear el texto a un lado de la forma.
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
    # Cree una Forma en línea, que servirá como contenedor para nuestro WordArt.
    # La forma solo puede ser una forma WordArt válida si le asignamos un ShapeType designado para WordArt.
    # Estos tipos tendrán "WordArt object" en la descripción,
    # y sus nombres de constantes enumeradoras comenzarán todos con "Text".
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

