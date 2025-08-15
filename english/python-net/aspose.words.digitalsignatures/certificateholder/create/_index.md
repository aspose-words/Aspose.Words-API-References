---
title: CertificateHolder.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.CertificateHolder.create method"
type: docs
weight: 20
url: /python-net/aspose.words.digitalsignatures/certificateholder/create/
---

## create(cert_bytes, password) {#bytes_str}

Creates [CertificateHolder](../) object using byte array of PKCS12 store and its password.



```python
def create(self, cert_bytes: bytes, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| cert_bytes | bytes | A byte array that contains data from an X.509 certificate. |
| password | str | The password required to access the X.509 certificate data. |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *certBytes* is``None`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``None`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |

## create(file_name, password) {#str_str}

Creates [CertificateHolder](../) object using path to PKCS12 store and its password.



```python
def create(self, file_name: str, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name of a certificate file. |
| password | str | The password required to access the X.509 certificate data. |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *fileName* is``None`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``None`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |

## create(file_name, password, alias) {#str_str_str}

Creates [CertificateHolder](../) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.



```python
def create(self, file_name: str, password: str, alias: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str | The name of a certificate file. |
| password | str | The password required to access the X.509 certificate data. |
| alias | str | The associated alias for a certificate and its private key |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *fileName* is``None`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``None`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |
| RuntimeError (Proxy error(SecurityException)) | Thrown if there is no private key with the given alias |

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

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [CertificateHolder](../)

