---
title: PdfDigitalSignatureDetails.hash_algorithm property
linktitle: hash_algorithm property
articleTitle: hash_algorithm property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.hash_algorithm property. Gets or sets the hash algorithm."
type: docs
weight: 30
url: /zh/python-net/aspose.words.saving/pdfdigitalsignaturedetails/hash_algorithm/
---

## PdfDigitalSignatureDetails.hash_algorithm property

Gets or sets the hash algorithm.


```python
@property
def hash_algorithm(self) -> aspose.words.saving.PdfDigitalSignatureHashAlgorithm:
    ...

@hash_algorithm.setter
def hash_algorithm(self, value: aspose.words.saving.PdfDigitalSignatureHashAlgorithm):
    ...

```

### Remarks

The default value is the SHA-256 algorithm.


### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 配置 "SaveOptions" 对象中的 "DigitalSignatureDetails" 对象，以
# 使用 "Save" 方法渲染时对文档进行数字签名。
signing_time = datetime.datetime(2015, 7, 20)
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'My Office', signing_time)
options.digital_signature_details.hash_algorithm = aw.saving.PdfDigitalSignatureHashAlgorithm.RIPE_MD160
self.assertEqual('Test Signing', options.digital_signature_details.reason)
self.assertEqual('My Office', options.digital_signature_details.location)
self.assertEqual(signing_time, options.digital_signature_details.signature_date.replace(tzinfo=None))
self.assertEqual(certificate_holder, options.digital_signature_details.certificate_holder)
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignature.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

