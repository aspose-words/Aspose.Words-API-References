---
title: PdfDigitalSignatureDetails.timestamp_settings property
linktitle: timestamp_settings property
articleTitle: timestamp_settings property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureDetails.timestamp_settings property. Gets or sets the digital signature timestamp settings."
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/pdfdigitalsignaturedetails/timestamp_settings/
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
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Создайте цифровую подпись и назначьте её нашему объекту SaveOptions, чтобы подписать документ при сохранении в PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# Создайте метку времени, проверенную службой временных меток.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# Срок жизни метки времени по умолчанию составляет 100 секунд.
# Мы можем установить период тайм‑аута через конструктор.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# Метод "Save" применит нашу подпись к выходному документу в этот момент.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureDetails](../)

