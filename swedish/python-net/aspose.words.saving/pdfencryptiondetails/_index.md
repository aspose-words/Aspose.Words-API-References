---
title: PdfEncryptionDetails class
linktitle: PdfEncryptionDetails class
articleTitle: PdfEncryptionDetails class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfEncryptionDetails class. Contains details for encrypting and access permissions for a PDF document"
type: docs
weight: 680
url: /sv/python-net/aspose.words.saving/pdfencryptiondetails/
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
# Utöka behörigheter för att tillåta redigering av annotationer.
encryption_details = aw.saving.PdfEncryptionDetails(user_password='password', owner_password='', permissions=aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY)
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
save_options = aw.saving.PdfSaveOptions()
# Aktivera kryptering via egenskapen "EncryptionDetails".
save_options.encryption_details = encryption_details
# När vi öppnar detta dokument måste vi ange lösenordet innan vi får åtkomst till dess innehåll.
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.EncryptionPermissions.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../)

