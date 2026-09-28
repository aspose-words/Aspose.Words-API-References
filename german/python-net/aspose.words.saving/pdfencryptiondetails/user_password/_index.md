---
title: PdfEncryptionDetails.user_password property
linktitle: user_password property
articleTitle: user_password property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.user_password property. Specifies the user password required for opening the encrypted PDF document."
type: docs
weight: 40
url: /de/python-net/aspose.words.saving/pdfencryptiondetails/user_password/
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

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

