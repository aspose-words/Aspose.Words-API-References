---
title: DigitalSignatureUtil.sign method
linktitle: sign method
articleTitle: sign method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.DigitalSignatureUtil.sign method"
type: docs
weight: 30
url: /python-net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
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
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Create a comment and date which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# Take an unsigned document from the local file system via a file stream,
# then create a signed copy of it determined by the filename of the output file stream.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

Shows how to add a signature line to a document, and then sign it using a digital certificate.

```python
def test_sign(self):

    signee_name = "Ron Williams"
    src_document_path = MY_DIR + "Document.docx"
    dst_document_path = ARTIFACTS_DIR + "SignDocumentCustom.sign.docx"
    certificate_path = MY_DIR + "morzal.pfx"
    certificate_password = "aw"

    for signee_info in self._create_signees():
        if signee_info.name == signee_name:
            self._sign_document(src_document_path, dst_document_path, signee_info, certificate_path,
                                certificate_password)
            break
    else:
        raise Exception("Signee does not exist.")

def _sign_document(self, src_document_path: str, dst_document_path: str,
                   signee_info, certificate_path: str, certificate_password: str):
    """Creates a copy of a source document signed using provided signee information and X509 certificate."""

    document = aw.Document(src_document_path)
    builder = aw.DocumentBuilder(document)

    # Configure and insert a signature line, an object in the document that will display a signature that we sign it with.
    signature_line_options = aw.SignatureLineOptions()
    signature_line_options.signer = signee_info.name
    signature_line_options.signer_title = signee_info.position

    signature_line = builder.insert_signature_line(signature_line_options).signature_line
    signature_line.id = signee_info.person_id

    # First, we will save an unsigned version of our document.
    builder.document.save(dst_document_path)

    certificate_holder = aw.digitalsignatures.CertificateHolder.create(certificate_path, certificate_password)

    sign_options = aw.digitalsignatures.SignOptions()
    sign_options.signature_line_id = signee_info.person_id
    sign_options.signature_line_image = signee_info.image

    # Overwrite the unsigned document we saved above with a version signed using the certificate.
    aw.digitalsignatures.DigitalSignatureUtil.sign(dst_document_path, dst_document_path, certificate_holder,
                                                   sign_options)

class Signee:

    def __init__(self, guid: uuid.UUID, name: str, position: str, image: bytes):
        self.person_id = guid
        self.name = name
        self.position = position
        self.image = image

def _create_signees(self):

    return [
        ExSignDocumentCustom.Signee(uuid.uuid4(), "Ron Williams", "Chief Executive Officer",
                                    self.image_to_byte_array(IMAGE_DIR + "Logo.jpg")),
        ExSignDocumentCustom.Signee(uuid.uuid4(), "Stephen Morse", "Head of Compliance",
                                    self.image_to_byte_array(IMAGE_DIR + "Logo.jpg"))
    ]
```

Shows how to sign documents with X.509 certificates.

```python
# Verify that a document is not signed.
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# There are two ways of saving a signed copy of a document to the local file system:
# 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - Take a document from a stream and save a signed copy to another stream.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# Please verify that all of the document's digital signatures are valid and check their details.
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

