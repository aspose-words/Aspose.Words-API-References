---
title: DigitalSignatureUtil.sign method
linktitle: sign method
articleTitle: sign method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.sign method"
type: docs
weight: 30
url: /de/python-net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---

## sign(src_stream, dst_stream, cert_holder, sign_options) {#bytesio_bytesio_certificateholder_signoptions}

Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/)
with digital signature and writes signed document to destination stream.
Supported formats are:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).

**Output will be written to the start of stream and stream size will be updated with content length.**





```python
def sign(self, src_stream: io.BytesIO, dst_stream: io.BytesIO, cert_holder: aspose.words.digitalsignatures.CertificateHolder, sign_options: aspose.words.digitalsignatures.SignOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_stream | io.BytesIO | The stream which contains the document to sign. |
| dst_stream | io.BytesIO | The stream that signed document will be written to. |
| cert_holder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| sign_options | [SignOptions](../../signoptions/) | [SignOptions](../../signoptions/) object with various signing options. |

## sign(src_file_name, dst_file_name, cert_holder, sign_options) {#str_str_certificateholder_signoptions}

Signs source document using given [CertificateHolder](../../certificateholder/) and [SignOptions](../../signoptions/)
with digital signature and writes signed document to destination file.
Supported formats are:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).




```python
def sign(self, src_file_name: str, dst_file_name: str, cert_holder: aspose.words.digitalsignatures.CertificateHolder, sign_options: aspose.words.digitalsignatures.SignOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_file_name | str | The file name of the document to sign. |
| dst_file_name | str | The file name of the signed document output. |
| cert_holder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |
| sign_options | [SignOptions](../../signoptions/) | [SignOptions](../../signoptions/) object with various signing options. |

## sign(src_stream, dst_stream, cert_holder) {#bytesio_bytesio_certificateholder}

Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature
and writes signed document to destination stream.
Supported formats are:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).

**Output will be written to the start of stream and stream size will be updated with content length.**





```python
def sign(self, src_stream: io.BytesIO, dst_stream: io.BytesIO, cert_holder: aspose.words.digitalsignatures.CertificateHolder):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_stream | io.BytesIO | The stream which contains the document to sign. |
| dst_stream | io.BytesIO | The stream that signed document will be written to. |
| cert_holder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## sign(src_file_name, dst_file_name, cert_holder) {#str_str_certificateholder}

Signs source document using given [CertificateHolder](../../certificateholder/) with digital signature
and writes signed document to destination file.
Supported formats are:
[LoadFormat.DOC](../../../aspose.words/loadformat/#DOC),
[LoadFormat.DOT](../../../aspose.words/loadformat/#DOT),
[LoadFormat.DOCX](../../../aspose.words/loadformat/#DOCX),
[LoadFormat.DOTX](../../../aspose.words/loadformat/#DOTX),
[LoadFormat.DOCM](../../../aspose.words/loadformat/#DOCM),
[LoadFormat.DOTM](../../../aspose.words/loadformat/#DOTM),
[LoadFormat.ODT](../../../aspose.words/loadformat/#ODT),
[LoadFormat.OTT](../../../aspose.words/loadformat/#OTT).




```python
def sign(self, src_file_name: str, dst_file_name: str, cert_holder: aspose.words.digitalsignatures.CertificateHolder):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_file_name | str | The file name of the document to sign. |
| dst_file_name | str | The file name of the signed document output. |
| cert_holder | [CertificateHolder](../../certificateholder/) | [CertificateHolder](../../certificateholder/) object with certificate that used to sign file. The certificate in holder MUST contain private keys and have the X509KeyStorageFlags.Exportable flag set. |

## Examples

Shows how to digitally sign documents.

```python
# Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Store, das einen privaten Schlüssel enthalten sollte.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# Nehmen Sie ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
# und erstellen Sie dann eine signierte Kopie davon, bestimmt durch den Dateinamen des Ausgabestreams.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

Shows how to sign a document with additional signing options.

```python
sign_options = aw.digitalsignatures.SignOptions()
sign_options.windows_version = '10.0'
sign_options.application_version = '16.0.19127'
sign_options.office_version = '16.0.19127/27'
sign_options.horizontal_resolution = 1024
sign_options.vertical_resolution = 768
sign_options.color_depth = 24
cert_bytes = system_helper.io.File.read_all_bytes(MY_DIR + 'morzal.pfx')
cert = aw.digitalsignatures.CertificateHolder.create(cert_bytes=cert_bytes, password='aw')
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Digitally signed.docx', dst_file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.docx', cert_holder=cert, sign_options=sign_options)
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'DigitalSignatureUtil.docx')
signature = signed_doc.digital_signatures[0]
self.assertEqual(1, signed_doc.digital_signatures.count)
self.assertTrue(signature.is_valid)
self.assertEqual('10.0', signature.windows_version)
self.assertEqual('16.0.19127', signature.application_version)
self.assertEqual('16.0.19127/27', signature.office_version)
self.assertEqual(1024, signature.horizontal_resolution)
self.assertEqual(768, signature.vertical_resolution)
self.assertEqual(24, signature.color_depth)
```

Shows how to sign documents with X.509 certificates.

```python
# Überprüfen Sie, dass ein Dokument nicht signiert ist.
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden werden.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
# 1 - Bezeichnen Sie ein Dokument mit einem lokalen Dateinamen und speichern Sie eine signierte Kopie an einem Ort, der durch einen anderen Dateinamen angegeben ist.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einen anderen Stream.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# Bitte überprüfen Sie, dass alle digitalen Signaturen des Dokuments gültig sind, und prüfen Sie deren Details.
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx')
digital_signature_collection = signed_doc.digital_signatures
self.assertTrue(digital_signature_collection.is_valid)
self.assertEqual(1, digital_signature_collection.count)
self.assertEqual(aw.digitalsignatures.DigitalSignatureType.XML_DSIG, digital_signature_collection[0].signature_type)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].issuer_name)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].subject_name)
```

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureUtil](../)

