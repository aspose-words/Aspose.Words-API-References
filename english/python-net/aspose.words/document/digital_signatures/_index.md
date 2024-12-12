---
title: Document.digital_signatures property
linktitle: digital_signatures property
articleTitle: digital_signatures property
second_title: Aspose.Words for Python
description: "Document.digital_signatures property. Gets the collection of digital signatures for this document and their validation results."
type: docs
weight: 110
url: /python-net/aspose.words/document/digital_signatures/
---

## Document.digital_signatures property

Gets the collection of digital signatures for this document and their validation results.


```python
@property
def digital_signatures(self) -> aspose.words.digitalsignatures.DigitalSignatureCollection:
    ...

```

### Remarks

This collection contains digital signatures that were loaded from the original document.
These digital signatures will not be saved when you save this [Document](../) object
into a file or stream because saving or converting will produce a document that is different from the
original and the original digital signatures will no longer be valid.

This collection is never ``None``. If the document is not signed, it will contain zero elements.




### Examples

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

Shows how to validate and display information about each signature in a document.

```python
doc = aw.Document(MY_DIR + 'Digitally signed.docx')
for signature in doc.digital_signatures:
    print(f"\n{('Valid' if signature.is_valid else 'Invalid')} signature: ")
    print(f'\tReason:\t{signature.comments}')
    print(f'\tType:\t{signature.signature_type}')
    print(f'\tSign time:\t{signature.sign_time}')
    # System.Security.Cryptography.X509Certificates.X509Certificate2 is not supported. That is why the following information is not accesible.
    #print(f"\tSubject name:\t{signature.certificate_holder.certificate.subject_name}")
    #print(f"\tIssuer name:\t{signature.certificate_holder.certificate.issuer_name.name}")
    print()
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

