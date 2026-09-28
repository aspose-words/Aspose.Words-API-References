---
title: PdfEncryptionDetails constructor
linktitle: PdfEncryptionDetails constructor
articleTitle: PdfEncryptionDetails constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails constructor"
type: docs
weight: 10
url: /fr/python-net/aspose.words.saving/pdfencryptiondetails/__init__/
---

## PdfEncryptionDetails(user_password, owner_password) {#str_str}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |

## PdfEncryptionDetails(user_password, owner_password, permissions) {#str_str_pdfpermissions}

Initializes an instance of this class.


```python
def __init__(self, user_password: str, owner_password: str, permissions: aspose.words.saving.PdfPermissions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| user_password | str |  |
| owner_password | str |  |
| permissions | [PdfPermissions](../../pdfpermissions/) |  |

## Examples

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

## See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

