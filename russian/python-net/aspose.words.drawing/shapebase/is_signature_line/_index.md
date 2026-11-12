---
title: ShapeBase.is_signature_line property
linktitle: is_signature_line property
articleTitle: is_signature_line property
second_title: Aspose.Words for Python
description: "ShapeBase.is_signature_line property. Indicates that shape is a [SignatureLine](../../signatureline/)."
type: docs
weight: 360
url: /ru/python-net/aspose.words.drawing/shapebase/is_signature_line/
---

## ShapeBase.is_signature_line property

Indicates that shape is a [SignatureLine](../../signatureline/).



```python
@property
def is_signature_line(self) -> bool:
    ...

```

### Examples

Shows how to create a line for a signature and insert it into a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
options = aw.SignatureLineOptions()
options.allow_comments = True
options.default_instructions = True
options.email = 'john.doe@management.com'
options.instructions = 'Please sign here'
options.show_date = True
options.signer = 'John Doe'
options.signer_title = 'Senior Manager'
# Вставьте фигуру, которая будет содержать строку подписи, внешний вид которой мы будем
# настраивать с помощью объекта "SignatureLineOptions", который мы создали выше.
# Если мы вставим фигуру, координаты которой начинаются в правом нижнем углу страницы,
# нам потребуется задать отрицательные координаты x и y, чтобы вывести фигуру в поле зрения.
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# Проверьте свойства нашей строки подписи через её объект Shape.
signature_line = shape.signature_line
self.assertEqual('john.doe@management.com', signature_line.email)
self.assertEqual('John Doe', signature_line.signer)
self.assertEqual('Senior Manager', signature_line.signer_title)
self.assertEqual('Please sign here', signature_line.instructions)
self.assertTrue(signature_line.show_date)
self.assertTrue(signature_line.allow_comments)
self.assertTrue(signature_line.default_instructions)
doc.save(file_name=ARTIFACTS_DIR + 'Shape.SignatureLine.docx')
```

### See Also

* module [aspose.words.drawing](../../)
* class [ShapeBase](../)

