---
title: PdfDigitalSignatureTimestampSettings.timeout property
linktitle: timeout property
articleTitle: timeout property
second_title: Aspose.Words for Python
description: "PdfDigitalSignatureTimestampSettings.timeout property. Time-out value for accessing timestamp server."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/pdfdigitalsignaturetimestampsettings/timeout/
---

## PdfDigitalSignatureTimestampSettings.timeout property

Time-out value for accessing timestamp server.


```python
@property
def timeout(self) -> datetime.timespan:
    ...

@timeout.setter
def timeout(self, value: datetime.timespan):
    ...

```

### Remarks

The default value is 100 seconds.


### Examples

Shows how to sign a saved PDF document digitally and timestamp it.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Signed PDF contents.')
# 创建一个可以传递给文档的 \"Save\" 方法的 \"PdfSaveOptions\" 对象
# 以修改该方法将文档转换为 .PDF 的方式。
options = aw.saving.PdfSaveOptions()
# 创建数字签名并将其分配给我们的 SaveOptions 对象，以在将文档保存为 PDF 时对其进行签名。
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
options.digital_signature_details = aw.saving.PdfDigitalSignatureDetails(certificate_holder, 'Test Signing', 'Aspose Office', datetime.datetime.now())
# 创建经时间戳授权机构验证的时间戳。
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword')
# 时间戳的默认寿命为 100 秒。
# 我们可以通过构造函数设置超时时间。
options.digital_signature_details.timestamp_settings = aw.saving.PdfDigitalSignatureTimestampSettings(server_url='https://freetsa.org/tsr', user_name='JohnDoe', password='MyPassword', timeout=datetime.timedelta(minutes=30))
self.assertEqual(1800.0, options.digital_signature_details.timestamp_settings.timeout.total_seconds)
self.assertEqual('https://freetsa.org/tsr', options.digital_signature_details.timestamp_settings.server_url)
self.assertEqual('JohnDoe', options.digital_signature_details.timestamp_settings.user_name)
self.assertEqual('MyPassword', options.digital_signature_details.timestamp_settings.password)
# "Save" 方法将在此时将我们的签名应用于输出文档。
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfDigitalSignatureTimestampSettings](../)

