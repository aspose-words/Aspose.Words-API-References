---
title: PdfEncryptionDetails class
linktitle: PdfEncryptionDetails class
articleTitle: PdfEncryptionDetails class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails class. Contains details for encrypting and access permissions for a PDF document"
type: docs
weight: 680
url: /de/python-net/aspose.words.saving/pdfencryptiondetails/
---

## PdfEncryptionDetails class

Contains details for encrypting and access permissions for a PDF document.
To learn more, visit the [Protect or Encrypt a Document](https://docs.aspose.com/words/python-net/protect-or-encrypt-a-document/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PdfEncryptionDetails(user_password, owner_password)](./__init__/#str_str) | Initializes an instance of this class. |
| [PdfEncryptionDetails(user_password, owner_password, permissions)](./__init__/#str_str_pdfpermissions) | Initializes an instance of this class. |

### Properties

| Name | Description |
| --- | --- |
| [owner_password](./owner_password/) | Specifies the owner password for the encrypted PDF document. |
| [permissions](./permissions/) | Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is [PdfPermissions.DISALLOW_ALL](../pdfpermissions/#DISALLOW_ALL). |
| [user_password](./user_password/) | Specifies the user password required for opening the encrypted PDF document. |

### Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Erweitern Sie die Berechtigungen, um das Bearbeiten von Anmerkungen zu ermöglichen.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Erstellen Sie ein "PdfSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
save_options = aw.saving.PdfSaveOptions()
# Aktivieren Sie die Verschlüsselung über die "EncryptionDetails"-Eigenschaft.
save_options.encryption_details = encryption_details
# Wenn wir dieses Dokument öffnen, müssen wir das Passwort angeben, bevor wir auf dessen Inhalt zugreifen können.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

