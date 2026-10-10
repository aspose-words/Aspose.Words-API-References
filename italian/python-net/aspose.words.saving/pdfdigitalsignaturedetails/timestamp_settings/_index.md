---
title: PdfDigitalSignatureDetails.timestamp_settings property
linktitle: timestamp_settings property
articleTitle: timestamp_settings property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.timestamp_settings property. Gets or sets the digital signature timestamp settings."
type: docs
weight: 70
url: /it/python-net/aspose.words.saving/pdfdigitalsignaturedetails/timestamp_settings/
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
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
options = aw.saving.PdfSaveOptions()
# Crea una firma digitale e assegnala al nostro oggetto SaveOptions per firmare il documento quando lo salviamo in PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Crea un timestamp verificato dall'autorità di timestamp.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# La durata predefinita del timestamp è di 100 secondi.
# Possiamo impostare il nostro periodo di timeout tramite il costruttore.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# Il metodo "Save" applicherà la nostra firma al documento di output in questo momento.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

