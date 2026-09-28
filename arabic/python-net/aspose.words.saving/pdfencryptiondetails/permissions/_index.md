---
title: PdfEncryptionDetails.permissions property
linktitle: permissions property
articleTitle: permissions property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.permissions property. Specifies the operations that are allowed to a user on an encrypted PDF document"
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/pdfencryptiondetails/permissions/
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
# قم بتمديد الأذونات للسماح بتحرير التعليقات التوضيحية.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
save_options = aw.saving.PdfSaveOptions()
# فعّل التشفير عبر الخاصية "EncryptionDetails".
save_options.encryption_details = encryption_details
# عند فتح هذا المستند، سنحتاج إلى تقديم كلمة المرور قبل الوصول إلى محتوياته.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

