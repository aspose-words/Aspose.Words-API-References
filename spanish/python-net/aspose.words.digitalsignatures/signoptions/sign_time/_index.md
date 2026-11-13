---
title: SignOptions.sign_time property
linktitle: sign_time property
articleTitle: sign_time property
second_title: Aspose.Words for Python
description: "SignOptions.sign_time property. The date of signing"
type: docs
weight: 90
url: /es/python-net/aspose.words.digitalsignatures/signoptions/sign_time/
---

## SignOptions.sign_time property

The date of signing.
Default value is **current time** (datetime.datetime.now)


```python
@property
def sign_time(self) -> datetime.datetime:
    ...

@sign_time.setter
def sign_time(self, value: datetime.datetime):
    ...

```

### Examples

Shows how to digitally sign documents.

```python
# Cree un certificado X.509 a partir de un almacén PKCS#12, que debe contener una clave privada.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Cree un comentario y una fecha que se aplicarán con nuestra nueva firma digital.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# Obtenga un documento sin firmar del sistema de archivos local mediante un flujo de archivo,
# luego cree una copia firmada del mismo determinada por el nombre de archivo del flujo de salida.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

