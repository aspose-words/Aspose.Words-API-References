---
title: FileFormatInfo.load_format property
linktitle: load_format property
articleTitle: load_format property
second_title: Aspose.Words for Python
description: "FileFormatInfo.load_format property. Gets the detected document format."
type: docs
weight: 50
url: /ru/python-net/aspose.words/fileformatinfo/load_format/
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

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Загрузите документ из файла без расширения и затем определите его формат.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Ниже представлены два метода преобразования LoadFormat в соответствующий SaveFormat.
    # 1 -  Получите строку расширения файла для LoadFormat, затем получите соответствующий SaveFormat из этой строки:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  Преобразуйте LoadFormat напрямую в его SaveFormat:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Загрузите документ из потока, а затем сохраните его с автоматически определённым расширением файла.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.is_encrypted](../is_encrypted/)

