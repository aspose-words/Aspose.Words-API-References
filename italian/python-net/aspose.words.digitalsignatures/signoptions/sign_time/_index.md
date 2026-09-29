---
title: SignOptions.sign_time property
linktitle: sign_time property
articleTitle: sign_time property
second_title: Aspose.Words for Python
description: "SignOptions.sign_time property. The date of signing"
type: docs
weight: 90
url: /it/python-net/aspose.words.digitalsignatures/signoptions/sign_time/
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
# Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Crea un commento e una data che saranno applicati con la nostra nuova firma digitale.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# Prendi un documento non firmato dal file system locale tramite uno stream di file,
# quindi crea una copia firmata di esso determinata dal nome file dello stream di output.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

