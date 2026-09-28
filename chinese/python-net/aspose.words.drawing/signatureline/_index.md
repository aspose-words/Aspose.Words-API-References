---
title: SignatureLine class
linktitle: SignatureLine class
articleTitle: SignatureLine class
second_title: Aspose.Words for Python
description: "aspose.words.drawing.SignatureLine class. Provides access to signature line properties"
type: docs
weight: 420
url: /zh/python-net/aspose.words.drawing/signatureline/
---

## SignatureLine class

Provides access to signature line properties.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [allow_comments](./allow_comments/) | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is ``False``. |
| [default_instructions](./default_instructions/) | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is ``True``. |
| [email](./email/) | Gets or sets suggested signer's e-mail address.  Default value for this property is **empty string** (). |
| [id](./id/) | Gets or sets identifier for this signature line. This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../aspose.words.digitalsignatures/digitalsignatureutil/). This value must be unique and by default it is randomly generated new Guid (). |
| [instructions](./instructions/) | Gets or sets instructions to the signer that are displayed on signing the signature line. This property is ignored if [SignatureLine.default_instructions](./default_instructions/) is set. Default value for this property is **empty string** (). |
| [is_signed](./is_signed/) | Indicates that signature line is signed by digital signature. |
| [is_valid](./is_valid/) | Indicates that signature line is signed by digital signature and this digital signature is valid. |
| [provider_id](./provider_id/) | Gets or sets signature provider identifier for this signature line. Default value is "{00000000-0000-0000-0000-000000000000}". |
| [show_date](./show_date/) | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is ``True``. |
| [signer](./signer/) | Gets or sets suggested signer of the signature line. Default value for this property is **empty string** (). |
| [signer_title](./signer_title/) | Gets or sets suggested signer's title (for example, Manager). Default value for this property is **empty string** (). |

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

* module [aspose.words.drawing](../)

