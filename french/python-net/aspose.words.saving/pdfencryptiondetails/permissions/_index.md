---
title: PdfEncryptionDetails.permissions property
linktitle: permissions property
articleTitle: permissions property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.permissions property. Specifies the operations that are allowed to a user on an encrypted PDF document"
type: docs
weight: 30
url: /fr/python-net/aspose.words.saving/pdfencryptiondetails/permissions/
---

## PdfEncryptionDetails.permissions property

Specifies the operations that are allowed to a user on an encrypted PDF document.
The default value is [PdfPermissions.DISALLOW_ALL](../../pdfpermissions/#DISALLOW_ALL).



```python
@property
def permissions(self) -> aspose.words.saving.PdfPermissions:
    ...

@permissions.setter
def permissions(self, value: aspose.words.saving.PdfPermissions):
    ...

```

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

