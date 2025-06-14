﻿---
title: PdfEncryptionDetails class
linktitle: PdfEncryptionDetails class
articleTitle: PdfEncryptionDetails class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails class. Contains details for encrypting and access permissions for a PDF document"
type: docs
weight: 670
url: /python-net/aspose.words.saving/pdfencryptiondetails/
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

* module [aspose.words.saving](../)

