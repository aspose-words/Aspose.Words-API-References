---
title: TextPath class
linktitle: TextPath class
articleTitle: TextPath class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.TextPath class. Defines the text and formatting of the text path (of a WordArt object)"
type: docs
weight: 480
url: /ru/python-net/aspose.words.drawing/textpath/
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
# Вставьте объект WordArt, чтобы отобразить текст в фигуре, которую мы можем изменять в размере и перемещать с помощью мыши в Microsoft Word.
# Укажите "ShapeType" в качестве аргумента, чтобы задать форму для WordArt.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Примените параметры форматирования "Bold" и "Italic" к тексту, используя соответствующие свойства.
shape.text_path.bold = True
shape.text_path.italic = True
# Ниже перечислены различные другие свойства, связанные с форматированием текста.
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
# Используйте свойство "On" для отображения/скрытия текста.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Используйте свойство "Kerning" для включения/выключения кернингового интервала между некоторыми символами.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# Используйте свойство "Spacing" для установки пользовательского интервала между символами по шкале от 0.0 (отсутствует) до 1.0 (по умолчанию).
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# Установите свойство "RotateLetters" в значение "true", чтобы повернуть каждый символ на 90 градусов против часовой стрелки.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# Установите свойство "SameLetterHeights" в значение "true", чтобы высота x каждого символа была равна высоте заглавных букв.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# По умолчанию размер текста всегда будет масштабироваться, чтобы соответствовать размеру содержащей фигуры, переопределяя настройку размера текста.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Если мы установим "FitShape: property" в значение "false", текст сохранит размер
# который задаётся свойством "Size", независимо от размера фигуры.
# Также используйте свойство "TextPathAlignment", чтобы выровнять текст к стороне фигуры.
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
    # Создайте встроенную Shape, которая будет служить контейнером для нашего WordArt.
    # Фигура может быть действительной фигурой WordArt только если мы назначим ей ShapeType, предназначенный для WordArt.
    # Эти типы будут иметь "WordArt object" в описании,
    # и их имена констант перечислителя будут начинаться с "Text".
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

