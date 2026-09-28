---
title: SignatureLine.signer property
linktitle: signer property
articleTitle: signer property
second_title: Aspose.Words for Python
description: "SignatureLine.signer property. Gets or sets suggested signer of the signature line"
type: docs
weight: 100
url: /zh/python-net/aspose.words.drawing/signatureline/signer/
---

## SignatureLine.signer property

Gets or sets suggested signer of the signature line.
Default value for this property is **empty string** ().



```python
@property
def signer(self) -> str:
    ...

@signer.setter
def signer(self, value: str):
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
# 插入一个将包含签名线的形状，其外观我们将
# 使用我们在上面创建的 "SignatureLineOptions" 对象进行自定义。
# 如果我们插入的形状坐标起始于页面的右下角，
# 我们需要提供负的 x 和 y 坐标以将形状显示出来。
shape = builder.insert_signature_line(signature_line_options=options, horz_pos=aw.drawing.RelativeHorizontalPosition.RIGHT_MARGIN, left=-170, vert_pos=aw.drawing.RelativeVerticalPosition.BOTTOM_MARGIN, top=-60, wrap_type=aw.drawing.WrapType.NONE)
self.assertTrue(shape.is_signature_line)
# 通过其 Shape 对象验证我们的签名线属性。
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
* class [SignatureLine](../)

