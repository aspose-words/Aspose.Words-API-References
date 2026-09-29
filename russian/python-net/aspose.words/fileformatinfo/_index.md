---
title: FileFormatInfo class
linktitle: FileFormatInfo class
articleTitle: FileFormatInfo class
second_title: Aspose.Words for Python
description: "aspose.words.FileFormatInfo class. Contains data returned by [FileFormatUtil](../fileformatutil/) document format detection methods"
type: docs
weight: 420
url: /ru/python-net/aspose.words/fileformatinfo/
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
# Настройте объект SaveOptions для шифрования документа
# с паролем при сохранении, а затем сохраните документ.
save_options = aw.saving.OdtSaveOptions(save_format=aw.SaveFormat.ODT)
save_options.password = 'MyPassword'
doc.save(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt', save_options=save_options)
# Проверьте тип файла нашего документа и его статус шифрования.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt')
self.assertEqual('.odt', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```python
# Используйте экземпляр FileFormatInfo, чтобы проверить, что документ не подписан цифровой подписью.
info = aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx')
self.assertEqual('.docx', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertFalse(info.has_digital_signature)
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx', cert_holder=certificate_holder, sign_options=sign_options)
# Используйте новый FileFormatInstance, чтобы подтвердить, что он подписан.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx')
self.assertTrue(info.has_digital_signature)
# Мы можем загрузить и получить доступ к подписьям подписанного документа в коллекции, как показано ниже.
self.assertEqual(1, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx').count)
```

### See Also

* module [aspose.words](../)

