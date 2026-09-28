---
title: PdfDigitalSignatureTimestampSettings constructor
linktitle: PdfDigitalSignatureTimestampSettings constructor
articleTitle: PdfDigitalSignatureTimestampSettings constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfDigitalSignatureTimestampSettings constructor"
type: docs
weight: 10
url: /ar/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/__init__/
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

## See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

