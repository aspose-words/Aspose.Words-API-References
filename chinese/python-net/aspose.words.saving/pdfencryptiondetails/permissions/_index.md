---
title: PdfEncryptionDetails.permissions property
linktitle: permissions property
articleTitle: permissions property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.permissions property. Specifies the operations that are allowed to a user on an encrypted PDF document"
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/pdfencryptiondetails/permissions/
---

## PdfEncryptionDetails.permissions property

Specifies the operations that are allowed to a user on an encrypted PDF document.
The default value is [PdfPermissions.DISALLOW_ALL](../../pdfpermissions/#DISALLOW_ALL).



```python
@property
def permissions(self) -> aspose.words.saving.PdfPermissions:
    ...

@permissions.setter
def permissions(self, value: aspose.words.saving.PdfPermissions):
    ...

```

### Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# 扩展权限以允许编辑批注。
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
save_options = aw.saving.PdfSaveOptions()
# 通过 "EncryptionDetails" 属性启用加密。
save_options.encryption_details = encryption_details
# 打开此文档时，需要在访问其内容之前提供密码。
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

