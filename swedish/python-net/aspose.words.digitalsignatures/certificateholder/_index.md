---
title: CertificateHolder class
linktitle: CertificateHolder class
articleTitle: CertificateHolder class
second_title: Aspose.Words for Python
description: "aspose.words.digitalsignatures.CertificateHolder class. Represents a holder of X509Certificate2 instance"
type: docs
weight: 10
url: /sv/python-net/aspose.words.digitalsignatures/certificateholder/
---

## CertificateHolder class

Represents a holder of **X509Certificate2** instance.
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/python-net/working-with-digital-signatures/) documentation article.




### Remarks

[CertificateHolder](./) can be created by static factory methods only. 
It contains an instance of **X509Certificate2** which is used to introduce private, public keys and certificate chains into the system.
This class is applied in [DigitalSignatureUtil](../digitalsignatureutil/) and [PdfDigitalSignatureDetails](../../aspose.words.saving/pdfdigitalsignaturedetails/) instead of obsolete methods with 
System.Security.Cryptography.X509Certificates.X509Certificate2 as parameters.




### Properties

| Name | Description |
| --- | --- |
| [certificate](./certificate/) | Returns the instance of **X509Certificate2** which holds private, public keys and certificate chain. |

### Methods

| Name | Description |
| --- | --- |
|[ create(cert_bytes, password)](./create/#bytes_str) | Creates [CertificateHolder](./) object using byte array of PKCS12 store and its password. |
|[ create(file_name, password)](./create/#str_str) | Creates [CertificateHolder](./) object using path to PKCS12 store and its password. |
|[ create(file_name, password, alias)](./create/#str_str_str) | Creates [CertificateHolder](./) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found. |

### Examples

Shows how to digitally sign documents.

```python
# Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'My comment'
sign_options.sign_time = datetime.datetime.now()
# Ta ett osignerat dokument från det lokala filsystemet via en filström,
# och skapa sedan en signerad kopia av den bestämd av filnamnet på utdatafilströmmen.
with system_helper.io.FileStream(MY_DIR + 'Document.docx', system_helper.io.FileMode.OPEN) as stream_in:
    with system_helper.io.FileStream(ARTIFACTS_DIR + 'DigitalSignatureUtil.SignDocument.docx', system_helper.io.FileMode.OPEN_OR_CREATE) as stream_out:
        aw.digitalsignatures.DigitalSignatureUtil.sign(src_stream=stream_in, dst_stream=stream_out, cert_holder=certificate_holder, sign_options=sign_options)
```

Shows how to sign encrypted document file.

```python
# Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Skapa en kommentar, ett datum och ett dekrypteringslösenord som kommer att tillämpas med vår nya digitala signatur.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
# Ange ett lokalt filnamn för det osignerade inmatningsdokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.DecryptionPassword.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../)

