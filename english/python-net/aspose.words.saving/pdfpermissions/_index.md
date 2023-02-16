---
title: PdfPermissions enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the operations that are allowed to a user on an encrypted PDF document."
type: docs
weight: 660
url: /python-net/aspose.words.saving/pdfpermissions/
---

## PdfPermissions enumeration

Specifies the operations that are allowed to a user on an encrypted PDF document.


### Members

| Name | Description |
| --- | --- |
| DISALLOW_ALL | Disallows all operations on the PDF document. This is the default value. |
| ALLOW_ALL | Allows all operations on the PDF document. |
| CONTENT_COPY | Copy or otherwise extract text and graphics from the document by operations other than that controlled by [PdfPermissions.CONTENT_COPY_FOR_ACCESSIBILITY](./#CONTENT_COPY_FOR_ACCESSIBILITY). |
| CONTENT_COPY_FOR_ACCESSIBILITY | Extract text and graphics (in support of accessibility to users with disabilities or for other purposes). |
| MODIFY_CONTENTS | Modify the contents of the document by operations other than those controlled by [PdfPermissions.MODIFY_ANNOTATIONS](./#MODIFY_ANNOTATIONS), [PdfPermissions.FILL_IN](./#FILL_IN), and [PdfPermissions.DOCUMENT_ASSEMBLY](./#DOCUMENT_ASSEMBLY). |
| MODIFY_ANNOTATIONS | Add or modify text annotations, fill in interactive form fields, and, if [PdfPermissions.MODIFY_CONTENTS](./#MODIFY_CONTENTS) is also set, create or modify interactive form fields (including signature fields). |
| FILL_IN | Fill in existing interactive form fields (including signature fields), even if [PdfPermissions.MODIFY_CONTENTS](./#MODIFY_CONTENTS) is clear. |
| DOCUMENT_ASSEMBLY | Assemble the document (insert, rotate, or delete pages and create document outline items or thumbnail images), even if [PdfPermissions.MODIFY_CONTENTS](./#MODIFY_CONTENTS) is clear. |
| PRINTING | Print the document (possibly not at the highest quality level, depending on whether [PdfPermissions.HIGH_RESOLUTION_PRINTING](./#HIGH_RESOLUTION_PRINTING) is also set). |
| HIGH_RESOLUTION_PRINTING | Print the document to a representation from which a faithful digital copy of the PDF content could be generated, based on an implementation-dependent algorithm. When this flag is clear (and [PdfPermissions.PRINTING](./#PRINTING) is set), printing shall be limited to a low-level representation of the appearance, possibly of degraded quality. |

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

* module [aspose.words.saving](../)

