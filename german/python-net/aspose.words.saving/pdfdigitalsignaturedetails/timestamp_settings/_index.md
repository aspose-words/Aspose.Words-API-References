---
title: PdfDigitalSignatureDetails.timestamp_settings property
linktitle: timestamp_settings property
articleTitle: timestamp_settings property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.timestamp_settings property. Gets or sets the digital signature timestamp settings."
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/pdfdigitalsignaturedetails/timestamp_settings/
---

## PdfDigitalSignatureDetails.timestamp_settings property

Gets or sets the digital signature timestamp settings.


```python
@property
def timestamp_settings(self) -> aspose.words.saving.PdfDigitalSignatureTimestampSettings:
    ...

@timestamp_settings.setter
def timestamp_settings(self, value: aspose.words.saving.PdfDigitalSignatureTimestampSettings):
    ...

```

### Remarks

The default value is ``None`` and the digital signature will not be time-stamped.
When this property is set to a valid [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/) object,
then the digital signature in the PDF document will be time-stamped.




### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Signed PDF contents.')
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
options = aw.saving.PdfSaveOptions()
# Erstellen Sie eine digitale Signatur und weisen Sie sie unserem SaveOptions‑Objekt zu, um das Dokument zu signieren, wenn wir es als PDF speichern.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Erstellen Sie einen von einer Zeitstempel‑Behörde verifizierten Zeitstempel.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# Die Standardlebensdauer des Zeitstempels beträgt 100 Sekunden.
# Wir können unsere Timeout‑Periode über den Konstruktor festlegen.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# Die Methode "Save" wird zu diesem Zeitpunkt unsere Signatur auf das Ausgabedokument anwenden.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

