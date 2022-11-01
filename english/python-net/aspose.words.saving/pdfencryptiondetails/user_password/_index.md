---
title: user_password property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the user password required for opening the encrypted PDF document."
type: docs
weight: 40
url: /python-net/aspose.words.saving/pdfencryptiondetails/user_password/
---

## PdfEncryptionDetails.user_password property

Specifies the user password required for opening the encrypted PDF document.

The user password will be required to open an encrypted PDF document for viewing. The permissions specified in 
[PdfEncryptionDetails.permissions](../permissions/) will be enforced by the reader software.

The user password can be ``None`` or empty string, in this case no password will be required from the user when 
opening the PDF document. The user password cannot be the same as the owner password.




### Examples

Shows how to set permissions on a saved PDF document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Hello world!")

encryption_details = aw.saving.PdfEncryptionDetails("password", "")

# Start by disallowing all permissions.
encryption_details.permissions = aw.saving.PdfPermissions.DISALLOW_ALL

# Extend permissions to allow the editing of annotations.
encryption_details.permissions = aw.saving.PdfPermissions.MODIFY_ANNOTATIONS | aw.saving.PdfPermissions.DOCUMENT_ASSEMBLY

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
save_options = aw.saving.PdfSaveOptions()

# Enable encryption via the "encryption_details" property.
save_options.encryption_details = encryption_details

# When we open this document, we will need to provide the password before accessing its contents.
doc.save(ARTIFACTS_DIR + "PdfSaveOptions.encryption_permissions.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfEncryptionDetails](../)

