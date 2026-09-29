---
title: PdfDigitalSignatureDetails.location property
linktitle: location property
articleTitle: location property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.location property. Gets or sets the location of the signing."
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/pdfdigitalsignaturedetails/location/
---

## PdfDigitalSignatureDetails.location property

Gets or sets the location of the signing.


```python
@property
def location(self) -> str:
    ...

@location.setter
def location(self, value: str):
    ...

```

### Remarks

The default value is ``None``.



### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Настройте объект "DigitalSignatureDetails" объекта "SaveOptions", чтобы
# цифрово подписать документ при его рендеринге методом "Save".
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

