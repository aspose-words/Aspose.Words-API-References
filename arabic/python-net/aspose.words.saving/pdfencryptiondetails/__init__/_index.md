---
title: PdfEncryptionDetails constructor
linktitle: PdfEncryptionDetails constructor
articleTitle: PdfEncryptionDetails constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails constructor"
type: docs
weight: 10
url: /ar/python-net/aspose.words.saving/pdfencryptiondetails/__init__/
---

## PdfEncryptionDetails(user_password, owner_password) {#str_str}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |

## PdfEncryptionDetails(user_password, owner_password, permissions) {#str_str_pdfpermissions}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str, permissions: aspose.words.saving.PdfPermissions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |
| permissions | [PdfPermissions](../../pdfpermissions/) |  |

## Examples

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

## See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

