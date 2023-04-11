---
title: create method
second_title: Aspose.Words for Python via .NET API Reference
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
| cert_bytes | bytes |  |
| password | str |  |

### Returns

An instance of [CertificateHolder](../)


### Exceptions

| exception | condition |
| --- | --- |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| System.Security.SecurityException | Thrown if PKCS12 store contains no aliases |
| System.IO.IOException | Thrown if there is wrong password or corrupted file. |

## create(file_name, password) {#str_str}

Creates [CertificateHolder](../) object using path to PKCS12 store and its password.



```python
def create(self, file_name: str, password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| password | str |  |

### Returns

An instance of [CertificateHolder](../)


### Exceptions

| exception | condition |
| --- | --- |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| System.Security.SecurityException | Thrown if PKCS12 store contains no aliases |
| System.IO.IOException | Thrown if there is wrong password or corrupted file. |

## create(file_name, password, alias) {#str_str_str}

Creates [CertificateHolder](../) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.



```python
def create(self, file_name: str, password: str, alias: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| file_name | str |  |
| password | str |  |
| alias | str |  |

### Returns

An instance of [CertificateHolder](../)


### Exceptions

| exception | condition |
| --- | --- |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| Org.BouncyCastle.Security.InvalidParameterException | Thrown if  is``None`` |
| System.Security.SecurityException | Thrown if PKCS12 store contains no aliases |
| System.IO.IOException | Thrown if there is wrong password or corrupted file. |
| System.Security.SecurityException | Thrown if there is no private key with the given alias |

## Examples

Shows how to create CertificateHolder objects.

```python
# Below are four ways of creating CertificateHolder objects.
# 1 -  Load a PKCS #12 file into a byte array and apply its password:
with open(MY_DIR + "morzal.pfx", "rb") as file:
    cert_bytes = file.read()
aw.digitalsignatures.CertificateHolder.create(cert_bytes, "aw")

# 2 -  Load a PKCS #12 file into a byte array, and apply a secure password:
password = NetworkCredential("", "aw").secure_password
aw.digitalsignatures.CertificateHolder.create(cert_bytes, password)

# If the certificate has private keys corresponding to aliases,
# we can use the aliases to fetch their respective keys. First, we will check for valid aliases.
with open(MY_DIR + "morzal.pfx", "rb") as cert_stream:
    pkcs12_store = Pkcs12Store(cert_stream, "aw").build()
    pkcs12_store.load(cert_stream, "aw")
    for alias in pkcs12_store.aliases:
        if pkcs12_store.is_key_entry(alias) and pkcs12_store.get_key(alias).key.is_private:
            print("Valid alias found:", alias)

# 3 -  Use a valid alias:
aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24")

# 4 -  Pass "null" as the alias in order to use the first available alias that returns a private key:
aw.digitalsignatures.CertificateHolder.create(MY_DIR + "morzal.pfx", "aw", None)
```

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

## See Also

* module [aspose.words.digitalsignatures](../../)
* class [CertificateHolder](../)

