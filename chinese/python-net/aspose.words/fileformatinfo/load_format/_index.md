---
title: FileFormatInfo.load_format property
linktitle: load_format property
articleTitle: load_format property
second_title: Aspose.Words for Python
description: "FileFormatInfo.load_format property. Gets the detected document format."
type: docs
weight: 50
url: /zh/python-net/aspose.words/fileformatinfo/load_format/
---

## FileFormatInfo.load_format property

Gets the detected document format.


```python
@property
def load_format(self) -> aspose.words.LoadFormat:
    ...

```

### Remarks

When an OOXML document is encrypted, it is not possible to ascertain whether it is
an Excel, Word or PowerPoint document without decrypting it first so for an encrypted OOXML
document this property will always return [LoadFormat.DOCX](../../loadformat/#DOCX).




### Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```python
doc = aw.Document()
# 配置 SaveOptions 对象以加密文档
# 在保存时使用密码，然后保存文档。
save_options = aw.saving.OdtSaveOptions(save_format=aw.SaveFormat.ODT)
save_options.password = 'MyPassword'
doc.save(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt', save_options=save_options)
# 验证文档的文件类型及其加密状态。
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt')
self.assertEqual('.odt', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```python
# 使用 FileFormatInfo 实例来验证文档未被数字签名。
info = aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx')
self.assertEqual('.docx', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertFalse(info.has_digital_signature)
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx', cert_holder=certificate_holder, sign_options=sign_options)
# 使用新的 FileFormatInstance 来确认它已签名。
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx')
self.assertTrue(info.has_digital_signature)
# 我们可以加载并在如下集合中访问已签名文档的签名。
self.assertEqual(1, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx').count)
```

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# 从缺少文件扩展名的文件加载文档，然后检测其文件格式。
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # 下面是两种将 LoadFormat 转换为相应 SaveFormat 的方法。
    # 1 - 获取 LoadFormat 的文件扩展名字符串，然后从该字符串获取相应的 SaveFormat：
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 - 将 LoadFormat 直接转换为其 SaveFormat：
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # 从流中加载文档，然后将其保存为自动检测的文件扩展名。
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.is_encrypted](../is_encrypted/)

