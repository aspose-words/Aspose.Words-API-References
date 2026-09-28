---
title: PdfDigitalSignatureTimestampSettings class
linktitle: PdfDigitalSignatureTimestampSettings class
articleTitle: PdfDigitalSignatureTimestampSettings class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp"
type: docs
weight: 670
url: /ar/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
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
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# أنشئ توقيعًا رقميًا وعيّنّه إلى كائن SaveOptions الخاص بنا لتوقيع المستند عند حفظه كملف PDF.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# أنشئ طابعًا زمنيًا تم التحقق منه من قبل سلطة الطابع الزمني.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# العمر الافتراضي للطابع الزمني هو 100 ثانية.
# يمكننا تعيين فترة المهلة الخاصة بنا عبر المُنشئ.
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# طريقة "Save" ستطبق توقيعنا على المستند الناتج في هذا الوقت.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

