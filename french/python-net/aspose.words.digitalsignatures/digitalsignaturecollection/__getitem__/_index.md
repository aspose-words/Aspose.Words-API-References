---
title: DigitalSignatureCollection indexer
linktitle: DigitalSignatureCollection indexer
articleTitle: DigitalSignatureCollection indexer
second_title: Aspose.Words for Python
description: "DigitalSignatureCollection indexer. Gets a document signature at the specified index."
type: docs
weight: 20
url: /fr/python-net/aspose.words.digitalsignatures/digitalsignaturecollection/__getitem__/
---

## \_\_getitem\_\_(index) {#int}

Gets a document signature at the specified index.


```python
def __getitem__(self, index: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### Examples

Shows how to sign documents with X.509 certificates.

```python
# Vérifiez qu'un document n'est pas signé.
self.assertFalse(aw.FileFormatUtil.detect_file_format(file_name=MY_DIR + 'Document.docx').has_digital_signature)
# Créez un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw', alias=None)
# Il existe deux manières d'enregistrer une copie signée d'un document sur le système de fichiers local :
# 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.sign_time = datetime.datetime.now()
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=MY_DIR + 'Document.docx', dst_file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx', cert_holder=certificate_holder, sign_options=sign_options)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# 2 - Prenez un document depuis un flux et enregistrez une copie signée vers un autre flux.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as in_doc:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'Document.DigitalSignature.docx', system_helper.io.FileMode.CREATE) as out_doc:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=in_doc, dst_stream=out_doc, cert_holder=certificate_holder)
self.assertTrue(aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'Document.DigitalSignature.docx').has_digital_signature)
# Veuillez vérifier que toutes les signatures numériques du document sont valides et consulter leurs détails.
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

