---
title: SignOptions.decryption_password property
linktitle: decryption_password property
articleTitle: decryption_password property
second_title: Aspose.Words for Python
description: "SignOptions.decryption_password property. The password to decrypt source document"
type: docs
weight: 50
url: /ar/python-net/aspose.words.digitalsignatures/signoptions/decryption_password/
---

## SignOptions.decryption_password property

The password to decrypt source document.
Default value is **empty string** ().



```python
@property
def decryption_password(self) -> str:
    ...

@decryption_password.setter
def decryption_password(self, value: str):
    ...

```

### Remarks

If OOXML document is encrypted, you should provide decryption password
to decrypt source document before it will be signed.
This is not required for documents in binary DOC format.


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

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

