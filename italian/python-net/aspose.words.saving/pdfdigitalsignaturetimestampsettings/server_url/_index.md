---
title: PdfDigitalSignatureTimestampSettings.server_url property
linktitle: server_url property
articleTitle: server_url property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureTimestampSettings.server_url property. Timestamp server URL."
type: docs
weight: 30
url: /it/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/server_url/
---

## PdfDigitalSignatureTimestampSettings.server_url property

Timestamp server URL.


```python
@property
def server_url(self) -> str:
    ...

@server_url.setter
def server_url(self, value: str):
    ...

```

### Remarks

The default value is ``None``.
If ``None``, then the digital signature will not be time-stamped.



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
* class [PdfDigitalSignatureTimestampSettings](../)

