---
title: TextPath.shadow property
linktitle: shadow property
articleTitle: shadow property
second_title: Aspose.Words for Python
description: "TextPath.shadow property. Defines whether a shadow is applied to the text on a text path."
type: docs
weight: 110
url: /tr/python-net/aspose.words.drawing/textpath/shadow/
---

## TextPath.shadow property

Defines whether a shadow is applied to the text on a text path.


```python
@property
def shadow(self) -> bool:
    ...

@shadow.setter
def shadow(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.




### Examples

Shows how to work with WordArt.

```python
doc = aw.Document()
# Microsoft Word'de fareyi kullanarak yeniden boyutlandırıp taşıyabileceğimiz bir şekil içinde metni göstermek için bir WordArt nesnesi ekleyin.
# WordArt için bir şekil ayarlamak üzere argüman olarak bir "ShapeType" sağlayın.
shape = ExShape._append_word_art(doc, 'Hello World! This text is bold, and italic.', 'Arial', 480, 24, aspose.pydrawing.Color.white, aspose.pydrawing.Color.black, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
# Metne, ilgili özellikleri kullanarak "Bold" ve "Italic" biçimlendirme ayarlarını uygulayın.
shape.text_path.bold = True
shape.text_path.italic = True
# Aşağıda çeşitli diğer metin biçimlendirme ile ilgili özellikler bulunmaktadır.
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
# Metni göstermek/gizlemek için "On" özelliğini kullanın.
shape = ExShape._append_word_art(doc, 'On set to "true"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = True
shape = ExShape._append_word_art(doc, 'On set to "false"', 'Calibri', 150, 24, aspose.pydrawing.Color.yellow, aspose.pydrawing.Color.purple, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.on = False
# Belirli karakterler arasındaki kerning aralığını etkinleştirmek/devre dışı bırakmak için "Kerning" özelliğini kullanın.
shape = ExShape._append_word_art(doc, 'Kerning: VAV', 'Times New Roman', 90, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = True
shape = ExShape._append_word_art(doc, 'No kerning: VAV', 'Times New Roman', 100, 24, aspose.pydrawing.Color.orange, aspose.pydrawing.Color.red, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
shape.text_path.kerning = False
# "Spacing" özelliğini kullanarak karakterler arasındaki özel aralığı 0.0 (yok) ile 1.0 (varsayılan) arasında bir ölçekle ayarlayın.
shape = ExShape._append_word_art(doc, 'Spacing set to 0.1', 'Calibri', 120, 24, aspose.pydrawing.Color.blue_violet, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_CASCADE_DOWN)
shape.text_path.spacing = 0.1
# "RotateLetters" özelliğini "true" olarak ayarlayarak her karakteri 90 derece saat yönünün tersine döndürün.
shape = ExShape._append_word_art(doc, 'RotateLetters', 'Calibri', 200, 36, aspose.pydrawing.Color.green_yellow, aspose.pydrawing.Color.green, aw.drawing.ShapeType.TEXT_WAVE)
shape.text_path.rotate_letters = True
# "SameLetterHeights" özelliğini "true" olarak ayarlayarak her karakterin x-yüksekliğinin büyük harf yüksekliğine eşit olmasını sağlayın.
shape = ExShape._append_word_art(doc, 'Same character height for lower and UPPER case', 'Calibri', 300, 24, aspose.pydrawing.Color.deep_sky_blue, aspose.pydrawing.Color.dodger_blue, aw.drawing.ShapeType.TEXT_SLANT_UP)
shape.text_path.same_letter_heights = True
# Varsayılan olarak, metnin boyutu her zaman içeren şeklin boyutuna uyması için ölçeklenir ve metin boyutu ayarını geçersiz kılar.
shape = ExShape._append_word_art(doc, 'FitShape on', 'Calibri', 160, 24, aspose.pydrawing.Color.light_blue, aspose.pydrawing.Color.blue, aw.drawing.ShapeType.TEXT_PLAIN_TEXT)
self.assertTrue(shape.text_path.fit_shape)
shape.text_path.size = 24
# Eğer "FitShape" özelliğini "false" olarak ayarlarsak, metin boyutunu korur
# bu, şeklin boyutundan bağımsız olarak "Size" özelliği tarafından belirlenir.
# Metni şeklin bir kenarına hizalamak için ayrıca "TextPathAlignment" özelliğini kullanın.
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
    # WordArt'ımız için bir kapsayıcı görevi görecek satır içi bir Shape oluşturun.
    # Shape, ona bir WordArt belirlenmiş ShapeType atadığımızda yalnızca geçerli bir WordArt şekli olabilir.
    # Bu tiplerin açıklamasında "WordArt object" bulunacaktır,
    # ve enumeratör sabit adları hepsi "Text" ile başlayacaktır.
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

