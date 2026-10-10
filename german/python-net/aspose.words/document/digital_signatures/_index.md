---
title: Document.digital_signatures property
linktitle: digital_signatures property
articleTitle: digital_signatures property
second_title: Aspose.Words for Python
description: "Document.digital_signatures property. Gets the collection of digital signatures for this document and their validation results."
type: docs
weight: 110
url: /de/python-net/aspose.words/document/digital_signatures/
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

### See Also

* module [aspose.words](../../)
* class [Document](../)

