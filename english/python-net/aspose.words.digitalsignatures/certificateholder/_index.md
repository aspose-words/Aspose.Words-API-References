﻿---
title: CertificateHolder class
linktitle: CertificateHolder class
articleTitle: CertificateHolder class
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.CertificateHolder class. Represents a holder of X509Certificate2 instance"
type: docs
weight: 10
url: /python-net/aspose.words.digitalsignatures/certificateholder/
---

## CertificateHolder class

Represents a holder of **X509Certificate2** instance.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




[CertificateHolder](./) can be created by static factory methods only. 
It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system.
This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with 
System.Security.Cryptography.X509Certificates.X509Certificate2 as parameters.




### Properties

| Name | Description |
| --- | --- |
| [certificate](./certificate/) | Returns the instance of **X509Certificate2** which holds private, public keys and certificate chain. |

### Methods

| Name | Description |
| --- | --- |
|[ create(cert_bytes, password)](./create/#bytes_str) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
|[ create(file_name, password)](./create/#str_str) | Creates [CertificateHolder](./) object using path to PKCS12 store and its password. |
|[ create(file_name, password, alias)](./create/#str_str_str) | Creates [CertificateHolder](./) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |

### Examples

Shows how to digitally sign documents.

```python
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

# Create a comment and date which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = "My comment"
sign_options.sign_time = datetime.now()

# Take an unsigned document from the local file system via a file stream,
# then create a signed copy of it determined by the filename of the output file stream.
with open(MY_DIR + "Document.docx", "rb") as stream_in:
    with open(ARTIFACTS_DIR + "DigitalSignatureUtil.sign_document.docx", "wb") as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(stream_in, stream_out, certificate_holder, sign_options)
```

Shows how to sign encrypted document file.

```python
# Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw")

# Create a comment, date, and decryption password which will be applied with our new digital signature.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = "Comment"
sign_options.sign_time = datetime.now()
sign_options.decryption_password = "docPassword"

# Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
input_file_name = MY_DIR + "Encrypted.docx"
output_file_name = ARTIFACTS_DIR + "DigitalSignatureUtil.decryption_password.docx"

aw.digitalsignatures.DigitalSignatureUtil.sign(input_file_name, output_file_name, certificate_holder, sign_options)
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
            self._sign_document(src_document_path, dst_document_path, signee_info, certificate_path, certificate_password)
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
    aw.digitalsignatures.DigitalSignatureUtil.sign(dst_document_path, dst_document_path, certificate_holder, sign_options)

def _image_to_byte_array(self, image_in: drawing.Image) -> bytes:
    """Converts an image to a byte array."""

    with io.BytesIO() as stream:
        image_in.save(stream, drawing.imaging.ImageFormat.png)
        return bytes(stream.getbuffer())

class Signee:

    def __init__(self, guid: uuid.UUID, name: str, position: str, image: bytes):
        self.person_id = guid
        self.name = name
        self.position = position
        self.image = image

def _create_signees(self):

    return [
        ExSignDocumentCustom.Signee(uuid.uuid4(), "Ron Williams", "Chief Executive Officer",
            self._image_to_byte_array(drawing.Image.from_file(IMAGE_DIR + "Logo.jpg"))),
        ExSignDocumentCustom.Signee(uuid.uuid4(), "Stephen Morse", "Head of Compliance",
            self._image_to_byte_array(drawing.Image.from_file(IMAGE_DIR + "Logo.jpg")))
    ]
```

### See Also

* module [aspose.words.digitalsignatures](../)

