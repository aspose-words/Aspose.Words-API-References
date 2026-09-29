---
title: PdfDigitalSignatureTimestampSettings constructor
linktitle: PdfDigitalSignatureTimestampSettings constructor
articleTitle: PdfDigitalSignatureTimestampSettings constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureTimestampSettings constructor"
type: docs
weight: 10
url: /tr/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/__init__/
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
# "PdfSaveOptions" nesnesi oluşturun; bu nesneyi belgenin "Save" metoduna geçebiliriz
# bu yöntemin belgeyi .PDF'ye nasıl dönüştürdüğünü değiştirmek için.
options = aw.saving.PdfSaveOptions()
# Bir dijital imza oluşturun ve belgeyi PDF olarak kaydettiğimizde imzalamak için SaveOptions nesnemize atayın.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Yetkili bir zaman damgası doğrulamalı zaman damgası oluşturun.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# Zaman damgasının varsayılan ömrü 100 saniyedir.
# Zaman aşımı süremizi yapıcı (constructor) aracılığıyla ayarlayabiliriz.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# "Save" yöntemi, bu aşamada imzamızı çıktı belgesine uygulayacaktır.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

## See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

