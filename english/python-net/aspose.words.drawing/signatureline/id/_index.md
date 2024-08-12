---
title: SignatureLine.id property
linktitle: id property
articleTitle: id property
second_title: Aspose.Words for Python
description: "SignatureLine.id property. Gets or sets identifier for this signature line"
type: docs
weight: 40
url: /python-net/aspose.words.drawing/signatureline/id/
---

## SignatureLine.id property

Gets or sets identifier for this signature line.
This identifier can be associated with a digital signature, when signing document using [DigitalSignatureUtil](../../../aspose.words.digitalsignatures/digitalsignatureutil/).
This value must be unique and by default it is randomly generated new Guid
().




```python
@property
def id(self) -> uuid.UUID:
    ...

@id.setter
def id(self, value: uuid.UUID):
    ...

```

### Examples

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

### See Also

* module [aspose.words.drawing](../../)
* class [SignatureLine](../)

