---
title: TextPath.text_path_alignment property
linktitle: text_path_alignment property
articleTitle: text_path_alignment property
second_title: Aspose.Words for Python
description: "TextPath.text_path_alignment property. Defines the alignment of text."
type: docs
weight: 170
url: /ar/python-net/aspose.words.drawing/textpath/text_path_alignment/
---

## TextPath.text_path_alignment property

Defines the alignment of text.


```python
@property
def text_path_alignment(self) -> aspose.words.drawing.TextPathAlignment:
    ...

@text_path_alignment.setter
def text_path_alignment(self, value: aspose.words.drawing.TextPathAlignment):
    ...

```

### Remarks

The default value is [TextPathAlignment.CENTER](../../textpathalignment/#CENTER).




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# أدرج كائن WordArt لعرض النص داخل شكل يمكننا تغيير حجمه وتحريكه باستخدام الفأرة في Microsoft Word.
# قدِّم "ShapeType" كمعامل لتعيين شكل لـ WordArt.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# طبق إعدادات التنسيق "Bold" و "Italic" على النص باستخدام الخصائص المعنية.
shape.text_path.bold = True
shape.text_path.italic = True
# فيما يلي مجموعة متنوعة من الخصائص المتعلقة بتنسيق النص.
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
# استخدم الخاصية "On" لإظهار/إخفاء النص.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# استخدم الخاصية "Kerning" لتمكين/تعطيل تباعد الحروف بين بعض الأحرف.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# استخدم الخاصية "Spacing" لتعيين التباعد المخصص بين الأحرف على مقياس من 0.0 (لا شيء) إلى 1.0 (افتراضي).
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# عيّن الخاصية "RotateLetters" إلى "true" لتدوير كل حرف 90 درجة عكس اتجاه عقارب الساعة.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# عيّن الخاصية "SameLetterHeights" إلى "true" لجعل ارتفاع x لكل حرف يساوي ارتفاع الحرف الكبير.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# بشكل افتراضي، سيُعدل حجم النص دائمًا ليتناسب مع حجم الشكل المحتوي، متجاوزًا إعداد حجم النص.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# إذا قمنا بتعيين الخاصية "FitShape" إلى "false"، سيبقى النص بالحجم
# الذي تحدده الخاصية "Size" بغض النظر عن حجم الشكل.
# استخدم الخاصية "TextPathAlignment" أيضًا لمحاذاة النص إلى جانب من الشكل.
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
    # أنشئ شكلًا مضمنًا، سيعمل كحاوية لـ WordArt الخاص بنا.
    # يمكن أن يكون الشكل شكل WordArt صالحًا فقط إذا قمنا بتعيين ShapeType مخصص لـ WordArt له.
    # هذه الأنواع ستحمل "WordArt object" في الوصف،
    # وأسماء الثوابت الخاصة بالعداد ستبدأ جميعها بـ "Text".
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

