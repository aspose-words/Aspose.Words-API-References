---
title: LoadOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for Python
description: "LoadOptions.password property. Gets or sets the password for opening an encrypted document"
type: docs
weight: 110
url: /ar/python-net/aspose.words.loading/loadoptions/password/
---

## LoadOptions.password property

Gets or sets the password for opening an encrypted document.
Can be ``None`` or empty string. Default is ``None``.



```python
@property
def password(self) -> str:
    ...

@password.setter
def password(self, value: str):
    ...

```

### Remarks

You need to know the password to open an encrypted document. If the document is not encrypted, set this to ``None`` or empty string.




### Examples

Shows how to sign encrypted document file.

```python
# أنشئ شهادة X.509 من مخزن PKCS#12، والذي يجب أن يحتوي على مفتاح خاص.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# أنشئ تعليقًا وتاريخًا وكلمة مرور فك التشفير التي سيتم تطبيقها مع توقيعنا الرقمي الجديد.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
# عيّن اسم ملف نظام محلي للمستند غير الموقّع كمدخل، واسم ملف إخراج لنسخته الموقّعة رقمياً الجديدة.
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.DecryptionPassword.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

