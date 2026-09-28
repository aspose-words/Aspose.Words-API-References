---
title: DigitalSignatureType enumeration
linktitle: DigitalSignatureType enumeration
articleTitle: DigitalSignatureType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureType enumeration. Specifies the type of a digital signature."
type: docs
weight: 50
url: /zh/python-net/aspose.words.digitalsignatures/digitalsignaturetype/
---

## DigitalSignatureType enumeration

Specifies the type of a digital signature.


### Members

| Name | Description |
| --- | --- |
| UNKNOWN | Indicates an error, unknown digital signature type. |
| CRYPTO_API | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| XML_DSIG | The XmlDsig signature method used in OOXML and OpenDocument documents. |

### Examples

Shows how to sign documents with X.509 certificates.

```python
# 验证文档未签名。
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# 从 PKCS12 文件创建 CertificateHolder 对象，我们将使用它来签署文档。
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# 有两种方法将文档的已签名副本保存到本地文件系统：
# 1 - 通过本地系统文件名指定文档，并将已签名副本保存到另一个文件名指定的位置。
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - 从流中获取文档并将已签名副本保存到另一个流。
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 请验证文档的所有数字签名均有效并检查其详细信息。
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx')
digital_signature_collection = signed_doc.digital_signatures
self.assertTrue(digital_signature_collection.is_valid)
self.assertEqual(1, digital_signature_collection.count)
self.assertEqual(aw.digitalsignatures.DigitalSignatureType.XML_DSIG, digital_signature_collection[0].signature_type)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].issuer_name)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].subject_name)
```

### See Also

* module [aspose.words.digitalsignatures](../)

