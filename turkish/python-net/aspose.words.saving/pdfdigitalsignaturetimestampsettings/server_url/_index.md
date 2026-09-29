---
title: PdfDigitalSignatureTimestampSettings.server_url property
linktitle: server_url property
articleTitle: server_url property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureTimestampSettings.server_url property. Timestamp server URL."
type: docs
weight: 30
url: /tr/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/server_url/
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

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

