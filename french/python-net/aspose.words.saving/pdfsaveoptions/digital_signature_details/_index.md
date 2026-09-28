---
title: PdfSaveOptions.digital_signature_details property
linktitle: digital_signature_details property
articleTitle: digital_signature_details property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.digital_signature_details property. Gets or sets the details for signing the output PDF document."
type: docs
weight: 80
url: /fr/python-net/aspose.words.saving/pdfsaveoptions/digital_signature_details/
---

## PdfSaveOptions.digital_signature_details property

Gets or sets the details for signing the output PDF document.


```python
@property
def digital_signature_details(self) -> aspose.words.saving.PdfDigitalSignatureDetails:
    ...

@digital_signature_details.setter
def digital_signature_details(self, value: aspose.words.saving.PdfDigitalSignatureDetails):
    ...

```

### Remarks

The default value is ``None`` and the output document will not be signed.
When this property is set to a valid [PdfDigitalSignatureDetails](../../pdfdigitalsignaturedetails/) object,
then the output PDF document will be digitally signed.




### Examples

Shows how to sign a generated PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Contents of signed PDF.')
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
options = aw.saving.PdfSaveOptions()
# Configurez l'objet "DigitalSignatureDetails" de l'objet "SaveOptions" pour
# signer numériquement le document lors de son rendu avec la méthode "Save".
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
* class [PdfSaveOptions](../)

