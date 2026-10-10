---
title: PdfEncryptionDetails.user_password property
linktitle: user_password property
articleTitle: user_password property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.user_password property. Specifies the user password required for opening the encrypted PDF document."
type: docs
weight: 40
url: /fr/python-net/aspose.words.saving/pdfencryptiondetails/user_password/
---

## PdfEncryptionDetails.user_password property

Specifies the user password required for opening the encrypted PDF document.


```python
@property
def user_password(self) -> str:
    ...

@user_password.setter
def user_password(self, value: str):
    ...

```

### Remarks

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in
[PdfEncryptionDetails.permissions](../permissions/) will be enforced by the reader software.

The user password can be ``None`` or empty string, in this case no password will be required from the user when
opening the PDF document. The user password cannot be the same as the owner password.




### Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Étendez les autorisations pour permettre la modification des annotations.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Créez un objet "PdfSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .PDF.
save_options = aw.saving.PdfSaveOptions()
# Activez le chiffrement via la propriété "EncryptionDetails".
save_options.encryption_details = encryption_details
# Lorsque nous ouvrons ce document, nous devrons fournir le mot de passe avant d'accéder à son contenu.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

