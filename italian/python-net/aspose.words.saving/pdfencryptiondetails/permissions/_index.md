---
title: PdfEncryptionDetails.permissions property
linktitle: permissions property
articleTitle: permissions property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.permissions property. Specifies the operations that are allowed to a user on an encrypted PDF document"
type: docs
weight: 30
url: /it/python-net/aspose.words.saving/pdfencryptiondetails/permissions/
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

