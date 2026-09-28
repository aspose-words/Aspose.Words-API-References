---
title: SignOptions.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for Python
description: "SignOptions.comments property. Specifies comments on the digital signature"
type: docs
weight: 40
url: /de/python-net/aspose.words.digitalsignatures/signoptions/comments/
---

## SignOptions.comments property

Specifies comments on the digital signature.
Default value is **empty string**().



```python
@property
def comments(self) -> str:
    ...

@comments.setter
def comments(self, value: str):
    ...

```

### Examples

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

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

