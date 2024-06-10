---
title: PdfDigitalSignatureTimestampSettings.user_name property
linktitle: user_name property
articleTitle: user_name property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureTimestampSettings.user_name property. Timestamp server user name."
type: docs
weight: 50
url: /python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/user_name/
---

## PdfDigitalSignatureTimestampSettings.user_name property

Timestamp server user name.


```python
@property
def user_name(self) -> str:
    ...

@user_name.setter
def user_name(self, value: str):
    ...

```

### Remarks

The default value is ``None``.



### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Signed PDF contents.')
# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + 'morzal.pfx', 'aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.now())
# Create a timestamp authority-verified timestamp.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings('https://freetsa.org/tsr', 'JohnDoe', 'MyPassword')
# The default lifespan of the timestamp is 100 seconds.
self.assertEqual(100.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds())
# We can set our timeout period via the constructor.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings('https://freetsa.org/tsr', 'JohnDoe', 'MyPassword', timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds())
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# The "save" method will apply our signature to the output document at this time.
doc.save(ARTIFACTS_DIR + 'PdfSaveOptions.pdf_digital_signature_timestamp.pdf', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

