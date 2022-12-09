---
title: get_UserPassword
second_title: Aspose.Words for C++ API Reference
description: Specifies the user password required for opening the encrypted PDF document.
type: docs
weight: 53
url: /cpp/aspose.words.saving/pdfencryptiondetails/get_userpassword/
---
## PdfEncryptionDetails::get_UserPassword method


Specifies the user password required for opening the encrypted PDF document.

```cpp
System::String Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword() const
```

## Remarks


The user password will be required to open an encrypted PDF document for viewing. The permissions specified in [Permissions](../get_permissions/) will be enforced by the reader software.

The user password can be **null** or empty string, in this case no password will be required from the user when opening the PDF document. The user password cannot be the same as the owner password.

## Examples



Shows how to set permissions on a saved PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto encryptionDetails = MakeObject<PdfEncryptionDetails>(u"password", String::Empty);

// Start by disallowing all permissions.
encryptionDetails->set_Permissions(PdfPermissions::DisallowAll);

// Extend permissions to allow the editing of annotations.
encryptionDetails->set_Permissions(PdfPermissions::ModifyAnnotations | PdfPermissions::DocumentAssembly);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Enable encryption via the "EncryptionDetails" property.
saveOptions->set_EncryptionDetails(encryptionDetails);

// When we open this document, we will need to provide the password before accessing its contents.
doc->Save(ArtifactsDir + u"PdfSaveOptions.EncryptionPermissions.pdf", saveOptions);
```

## See Also

* Class [PdfEncryptionDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
