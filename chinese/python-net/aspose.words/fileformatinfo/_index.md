---
title: FileFormatInfo class
linktitle: FileFormatInfo class
articleTitle: FileFormatInfo class
second_title: Aspose.Words for Python
description: "aspose.words.FileFormatInfo class. Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods"
type: docs
weight: 420
url: /zh/python-net/aspose.words/fileformatinfo/
---

## FileFormatInfo class

Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods.
To learn more, visit the [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/python-net/detect-file-format-and-check-format-compatibility/) documentation article.




### Remarks

You do not create instances of this class directly. Objects of this class are returned by
[FileFormatUtil.detect_file_format()](../fileformatutil/detect_file_format/#bytesio) methods.




### Properties

| Name | Description |
| --- | --- |
| [encoding](./encoding/) | Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents. |
| [has_digital_signature](./has_digital_signature/) | Returns ``True`` if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not  specify whether the signature is valid or not. |
| [has_macros](./has_macros/) | Returns ``True`` if this document contains a VBA macros. |
| [is_encrypted](./is_encrypted/) | Returns ``True`` if the document is encrypted and requires a password to open. |
| [load_format](./load_format/) | Gets the detected document format. |

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

### See Also

* module [aspose.words](../)

