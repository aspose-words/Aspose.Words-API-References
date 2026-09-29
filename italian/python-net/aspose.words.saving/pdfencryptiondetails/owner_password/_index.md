---
title: PdfEncryptionDetails.owner_password property
linktitle: owner_password property
articleTitle: owner_password property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.owner_password property. Specifies the owner password for the encrypted PDF document."
type: docs
weight: 20
url: /it/python-net/aspose.words.saving/pdfencryptiondetails/owner_password/
---

## PdfEncryptionDetails.owner_password property

Specifies the owner password for the encrypted PDF document.


```python
@property
def owner_password(self) -> str:
    ...

@owner_password.setter
def owner_password(self, value: str):
    ...

```

### Remarks

The owner password allows the user to open an encrypted PDF document without any access restrictions
specified in [PdfEncryptionDetails.permissions](../permissions/).

The owner password cannot be the same as the user password.




### Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Estendi i permessi per consentire la modifica delle annotazioni.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
# per modificare il modo in cui quel metodo converte il documento in .PDF.
save_options = aw.saving.PdfSaveOptions()
# Abilita la crittografia tramite la proprietà "EncryptionDetails".
save_options.encryption_details = encryption_details
# Quando apriamo questo documento, dovremo fornire la password prima di accedere al suo contenuto.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

