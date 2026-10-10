---
title: DigitalSignatureCollection.is_valid property
linktitle: is_valid property
articleTitle: is_valid property
second_title: Aspose.Words for Python
description: "DigitalSignatureCollection.is_valid property. Returns ``True`` if all digital signatures in this collection are valid and the document has not been tampered with Also returns ``True`` if there are no digital signatures"
type: docs
weight: 40
url: /es/python-net/aspose.words.digitalsignatures/digitalsignaturecollection/is_valid/
---

## DigitalSignatureCollection.is_valid property

Returns ``True`` if all digital signatures in this collection are valid and the document has not been tampered with
Also returns ``True`` if there are no digital signatures.
Returns ``False`` if at least one digital signature is invalid.



```python
@property
def is_valid(self) -> bool:
    ...

```

### Examples

Shows how to sign documents with X.509 certificates.

```python
# Verifique que un documento no esté firmado.
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# Cree un objeto CertificateHolder a partir de un archivo PKCS12, que utilizaremos para firmar el documento.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
# 1 - Designe un documento mediante un nombre de archivo del sistema local y guarde una copia firmada en una ubicación especificada por otro nombre de archivo.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - Tome un documento de un flujo y guarde una copia firmada en otro flujo.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# Por favor, verifique que todas las firmas digitales del documento sean válidas y revise sus detalles.
signed_doc = aw.Document(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx')
digital_signature_collection = signed_doc.digital_signatures
self.assertTrue(digital_signature_collection.is_valid)
self.assertEqual(1, digital_signature_collection.count)
self.assertEqual(aw.digitalsignatures.DigitalSignatureType.XML_DSIG, digital_signature_collection[0].signature_type)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].issuer_name)
self.assertEqual('CN=Morzal.Me', signed_doc.digital_signatures[0].subject_name)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [DigitalSignatureCollection](../)

