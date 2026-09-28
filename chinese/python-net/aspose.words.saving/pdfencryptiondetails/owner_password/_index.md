---
title: PdfEncryptionDetails.owner_password property
linktitle: owner_password property
articleTitle: owner_password property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.owner_password property. Specifies the owner password for the encrypted PDF document."
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/pdfencryptiondetails/owner_password/
---

## PdfEncryptionDetails.owner_password property

Specifies the owner password for the encrypted PDF document.


```python
@property
def owner_password(self) -> str:
    ...

@owner_password.setter
def owner_password(self, value: str):
    ...

```

### Remarks

The owner password allows the user to open an encrypted PDF document without any access restrictions
specified in [PdfEncryptionDetails.permissions](../permissions/).

The owner password cannot be the same as the user password.




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

