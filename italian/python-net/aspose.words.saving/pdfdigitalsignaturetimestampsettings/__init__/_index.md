---
title: PdfDigitalSignatureTimestampSettings constructor
linktitle: PdfDigitalSignatureTimestampSettings constructor
articleTitle: PdfDigitalSignatureTimestampSettings constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureTimestampSettings constructor"
type: docs
weight: 10
url: /it/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/__init__/
---

## PdfDigitalSignatureTimestampSettings() {#default}

Initializes an instance of this class.


```python
def __init__(self):
    ...
```

## PdfDigitalSignatureTimestampSettings(server_url, user_name, password) {#str_str_str}

Initializes an instance of this class.


```python
def __init__(self, server_url: str, user_name: str, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| server_url | str | Timestamp server URL. |
| user_name | str | Timestamp server user name. |
| password | str | Timestamp server password. |

## PdfDigitalSignatureTimestampSettings(server_url, user_name, password, timeout) {#str_str_str_timespan}

Initializes an instance of this class.


```python
def __init__(self, server_url: str, user_name: str, password: str, timeout: datetime.timespan):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| server_url | str | Timestamp server URL. |
| user_name | str | Timestamp server user name. |
| password | str | Timestamp server password. |
| timeout | datetime.timespan | Time-out value for accessing timestamp server. |

## Examples

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

## See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

