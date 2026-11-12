---
title: FileFormatUtil.detect_file_format method
linktitle: detect_file_format method
articleTitle: detect_file_format method
second_title: Aspose.Words for Python
description: "aspose.words.FileFormatUtil.detect_file_format method"
type: docs
weight: 30
url: /tr/python-net/aspose.words/fileformatutil/detect_file_format/
---

## detect_file_format(file_name) {#str}

Detects and returns the information about a format of a document stored in a disk file.


```python
def detect_file_format(self, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The file name. |

### Remarks

Even if this method detects the document format, it does not guarantee
that the specified document is valid. This method only detects the document format by
reading data that is sufficient for detection. To fully verify that a document is valid
you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is
recognized, but the detection cannot complete because of corruption.




### Returns

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.


## detect_file_format(stream) {#bytesio}

Detects and returns the information about a format of a document stored in a stream.


```python
def detect_file_format(self, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | io.BytesIO | The stream. |

### Remarks

The stream must be positioned at the beginning of the document.

When this method returns, the position in the stream is restored to the original position.

Even if this method detects the document format, it does not guarantee
that the specified document is valid. This method only detects the document format by
reading data that is sufficient for detection. To fully verify that a document is valid
you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is
recognized, but the detection cannot complete because of corruption.




### Returns

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.


## Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```python
doc = aw.Document()
# Belgeyi şifrelemek için bir SaveOptions nesnesi yapılandırın
# kaydederken bir şifreyle ve ardından belgeyi kaydedin.
save_options = aw.saving.OdtSaveOptions(save_format=aw.SaveFormat.ODT)
save_options.password = 'MyPassword'
doc.save(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt', save_options=save_options)
# Belgemizin dosya türünü ve şifreleme durumunu doğrulayın.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt')
self.assertEqual('.odt', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

Shows how to use the FileFormatUtil class to detect the document format and presence of digital signatures.

```python
# Bir FileFormatInfo örneği kullanarak bir belgenin dijital olarak imzalanmadığını doğrulayın.
info = aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx')
self.assertEqual('.docx', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertFalse(info.has_digital_signature)
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx', cert_holder=certificate_holder, sign_options=sign_options)
# Yeni bir FileFormatInstance kullanarak imzalı olduğunu onaylayın.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx')
self.assertTrue(info.has_digital_signature)
# İmzalı bir belgenin imzalarını bu şekilde bir koleksiyonda yükleyebilir ve erişebiliriz.
self.assertEqual(1, aw.digitalsignatures.DigitalSignatureUtil.load_signatures(file_name=ARTIFACTS_DIR + 'File.DetectDigitalSignatures.docx').count)
```

Shows how to use the FileFormatUtil methods to detect the format of a document.

```python
# Dosya uzantısı olmayan bir dosyadan belge yükleyin ve ardından dosya formatını tespit edin.
with system_helper.io.File.open_read(MY_DIR + 'Word document with missing file extension') as doc_stream:
    info = aw.FileFormatUtil.detect_file_format(stream=doc_stream)
    load_format = info.load_format
    self.assertEqual(aw.LoadFormat.DOC, load_format)
    # Aşağıda bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi verilmiştir.
    # 1 -  LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden ilgili SaveFormat'ı alın:
    file_extension = aw.FileFormatUtil.load_format_to_extension(load_format)
    save_format = aw.FileFormatUtil.extension_to_save_format(file_extension)
    # 2 -  LoadFormat'ı doğrudan SaveFormat'ına dönüştürün:
    save_format = aw.FileFormatUtil.load_format_to_save_format(load_format)
    # Bir belgeyi akıştan yükleyin ve ardından otomatik olarak algılanan dosya uzantısına kaydedin.
    doc = aw.Document(stream=doc_stream)
    self.assertEqual('.doc', aw.FileFormatUtil.save_format_to_extension(save_format))
    doc.save(file_name=ARTIFACTS_DIR + 'File.SaveToDetectedFileFormat' + aw.FileFormatUtil.save_format_to_extension(save_format))
```

## See Also

* module [aspose.words](../../)
* class [FileFormatUtil](../)

