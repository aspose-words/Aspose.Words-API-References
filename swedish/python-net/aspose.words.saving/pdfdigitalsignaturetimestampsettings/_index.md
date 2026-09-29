---
title: PdfDigitalSignatureTimestampSettings class
linktitle: PdfDigitalSignatureTimestampSettings class
articleTitle: PdfDigitalSignatureTimestampSettings class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp"
type: docs
weight: 670
url: /sv/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---

## PdfDigitalSignatureTimestampSettings class

Contains settings of the digital signature timestamp.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PdfDigitalSignatureTimestampSettings()](./__init__/#default) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(server_url, user_name, password)](./__init__/#str_str_str) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings(server_url, user_name, password, timeout)](./__init__/#str_str_str_timespan) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [password](./password/) | Timestamp server password. |
| [server_url](./server_url/) | Timestamp server URL. |
| [timeout](./timeout/) | Time-out value for accessing timestamp server. |
| [user_name](./user_name/) | Timestamp server user name. |

### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Signed PDF contents.')
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Skapa en digital signatur och tilldela den till vårt SaveOptions‑objekt för att signera dokumentet när vi sparar det till PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Skapa en tidsstämpel som verifierats av en tidsstämpelauktoritet.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# Standardlivslängden för tidsstämpeln är 100 sekunder.
# Vi kan ställa in vår timeout‑period via konstruktorn.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# Metoden "Save" kommer att applicera vår signatur på utdata‑dokumentet vid detta tillfälle.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

