---
title: SignOptions.decryption_password property
linktitle: decryption_password property
articleTitle: decryption_password property
second_title: Aspose.Words for Python
description: "SignOptions.decryption_password property. The password to decrypt source document"
type: docs
weight: 50
url: /fr/python-net/aspose.words.digitalsignatures/signoptions/decryption_password/
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
# Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
certificate_holder = aw.digitalsignatures.CertificateHolder.create(file_name=MY_DIR + 'morzal.pfx', password='aw')
# Créez un commentaire, une date et un mot de passe de déchiffrement qui seront appliqués avec notre nouvelle signature numérique.
sign_options = aw.digitalsignatures.SignOptions()
sign_options.comments = 'Comment'
sign_options.sign_time = datetime.datetime.now()
sign_options.decryption_password = 'docPassword'
# Définissez un nom de fichier système local pour le document d'entrée non signé, et un nom de fichier de sortie pour sa nouvelle copie numériquement signée.
input_file_name = MY_DIR + 'Encrypted.docx'
output_file_name = ARTIFACTS_DIR + 'DigitalSignatureUtil.DecryptionPassword.docx'
aw.digitalsignatures.DigitalSignatureUtil.sign(src_file_name=input_file_name, dst_file_name=output_file_name, cert_holder=certificate_holder, sign_options=sign_options)
```

### See Also

* module [aspose.words.digitalsignatures](../../)
* class [SignOptions](../)

