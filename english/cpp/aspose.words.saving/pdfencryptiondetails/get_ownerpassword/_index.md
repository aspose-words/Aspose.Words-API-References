---
title: get_OwnerPassword
second_title: Aspose.Words for C++ API Reference
description: Specifies the owner password for the encrypted PDF document.
type: docs
weight: 14
url: /cpp/aspose.words.saving/pdfencryptiondetails/get_ownerpassword/
---
## PdfEncryptionDetails.get_OwnerPassword method


Specifies the owner password for the encrypted PDF document.

```cpp
System::String Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword() const
```


The owner password allows the user to open an encrypted PDF document without any access restrictions specified in [Permissions](../get_permissions/).

The owner password cannot be the same as the user password.

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

