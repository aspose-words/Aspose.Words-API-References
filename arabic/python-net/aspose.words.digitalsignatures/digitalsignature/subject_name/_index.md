---
title: DigitalSignature.subject_name property
linktitle: subject_name property
articleTitle: subject_name property
second_title: Aspose.Words for Python
description: "DigitalSignature.subject_name property. Returns the subject distinguished name of the certificate that was used to sign the document."
type: docs
weight: 120
url: /ar/python-net/aspose.words.digitalsignatures/digitalsignature/subject_name/
---

## DigitalSignature.subject_name property

Returns the subject distinguished name of the certificate that was used to sign the document.


```python
@property
def subject_name(self) -> str:
    ...

```

### Examples

Shows how to sign documents with X.509 certificates.

```python
# تحقق من أن المستند غير موقّع.
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# أنشئ كائن CertificateHolder من ملف PKCS12، والذي سنستخدمه لتوقيع المستند.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# هناك طريقتان لحفظ نسخة موقّعة من المستند على نظام الملفات المحلي:
# 1 - عيّن مستندًا باسم ملف نظام محلي واحفظ نسخة موقّعة في موقع يحدده اسم ملف آخر.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - خذ مستندًا من تدفق واحفظ نسخة موقّعة إلى تدفق آخر.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# يرجى التحقق من أن جميع توقيعات المستند الرقمية صالحة وتفقد تفاصيلها.
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx')
digital_signature_collection = signed_doc.digital_signatures
self.assertTrue(digital_signature_collection.is_valid)
self.assertEqual(1, digital_signature_collection.count)
self.assertEqual(aw.digitalsignatures.DigitalSignatureType.XML_DSIG, digital_signature_collection[0].signature_type)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].issuer_name)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].subject_name)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignature](../)

