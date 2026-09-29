---
title: SignOptions.decryption_password property
linktitle: decryption_password property
articleTitle: decryption_password property
second_title: Aspose.Words for Python
description: "SignOptions.decryption_password property. The password to decrypt source document"
type: docs
weight: 50
url: /tr/python-net/aspose.words.digitalsignatures/signoptions/decryption_password/
---

## SignOptions.decryption_password property

The password to decrypt source document.
Default value is **empty string** ().



```python
@property
def decryption_password(self) -> str:
    ...

@decryption_password.setter
def decryption_password(self, value: str):
    ...

```

### Remarks

If OOXML document is encrypted, you should provide decryption password
to decrypt source document before it will be signed.
This is not required for documents in binary DOC format.


### Examples

Shows how to sign encrypted document file.

```python
# Özel bir anahtar içermesi gereken bir PKCS#12 deposundan X.509 sertifikası oluşturun.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme parolası oluşturun.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
# İmzasız giriş belgesi için yerel sistem dosya adı ve yeni dijital olarak imzalanmış kopyası için bir çıktı dosya adı ayarlayın.
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.DecryptionPassword.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

