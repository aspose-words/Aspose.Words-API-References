﻿---
title: PdfEncryptionDetails.owner_password property
linktitle: owner_password property
articleTitle: owner_password property
second_title: Aspose.Words for Python
description: "PdfEncryptionDetails.owner_password property. Specifies the owner password for the encrypted PDF document."
type: docs
weight: 20
url: /python-net/aspose.words.saving/pdfencryptiondetails/owner_password/
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
# Extend permissions to allow the editing of annotations.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()
# Enable encryption via the "EncryptionDetails" property.
save_options.encryption_details = encryption_details
# When we open this document, we will need to provide the password before accessing its contents.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

