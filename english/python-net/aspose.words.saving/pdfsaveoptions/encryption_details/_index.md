---
title: PdfSaveOptions.encryption_details property
linktitle: encryption_details property
articleTitle: encryption_details property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.encryption_details property. Gets or sets the details for encrypting the output PDF document."
type: docs
weight: 130
url: /python-net/aspose.words.saving/pdfsaveoptions/encryption_details/
---

## PdfSaveOptions.encryption_details property

Gets or sets the details for encrypting the output PDF document.


```python
@property
def encryption_details(self) -> aspose.words.saving.PdfEncryptionDetails:
    ...

@encryption_details.setter
def encryption_details(self, value: aspose.words.saving.PdfEncryptionDetails):
    ...

```

### Remarks

The default value is ``None`` and the output document will not be encrypted.
When this property is set to a valid [PdfEncryptionDetails](../../pdfencryptiondetails/) object,
then the output PDF document will be encrypted.

AES-128 encryption algorithm is used when saving to PDF 1.7 based compliance (including PDF/UA-1).
AES-256 encryption algorithm is used when saving to PDF 2.0 based compliance.

Encryption is prohibited by PDF/A compliance. This option will be ignored when saving to PDF/A.

[PdfPermissions.CONTENT_COPY_FOR_ACCESSIBILITY](../../pdfpermissions/#CONTENT_COPY_FOR_ACCESSIBILITY) permission is required by PDF/UA compliance
if the output document is encrypted. This permission will automatically used when saving to PDF/UA.

[PdfPermissions.CONTENT_COPY_FOR_ACCESSIBILITY](../../pdfpermissions/#CONTENT_COPY_FOR_ACCESSIBILITY) permission is deprecated in PDF 2.0 format.
This permission will be ignored when saving to PDF 2.0.




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
* class [PdfSaveOptions](../)

