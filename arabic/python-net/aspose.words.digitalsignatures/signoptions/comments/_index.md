---
title: SignOptions.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Python
description: "SignOptions.comments property. Specifies comments on the digital signature"
type: docs
weight: 40
url: /ar/python-net/aspose.words.digitalsignatures/signoptions/comments/
---

## SignOptions.comments property

Specifies comments on the digital signature.
Default value is **empty string**().



```python
@property
def comments(self) -> str:
    ...

@comments.setter
def comments(self, value: str):
    ...

```

### Examples

Shows how to digitally sign documents.

```python
# أنشئ شهادة X.509 من مخزن PKCS#12، والذي يجب أن يحتوي على مفتاح خاص.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# أنشئ تعليقًا وتاريخًا سيتم تطبيقهما مع توقيعنا الرقمي الجديد.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# خذ مستندًا غير موقّع من نظام الملفات المحلي عبر تدفق ملف،
# ثم أنشئ نسخة موقّعة منه يتم تحديدها باسم ملف تدفق الإخراج.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

