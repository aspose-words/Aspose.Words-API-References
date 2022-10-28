---
title: PdfEncryptionDetails
second_title: Aspose.Words for C++ API Reference
description: Contains details for encrypting and access permissions for a PDF document.
type: docs
weight: 300
url: /cpp/aspose.words.saving/pdfencryptiondetails/
---
## PdfEncryptionDetails class


Contains details for encrypting and access permissions for a PDF document.

```cpp
class PdfEncryptionDetails : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_OwnerPassword](./get_ownerpassword/)() const | Specifies the owner password for the encrypted PDF document. |
| [get_Permissions](./get_permissions/)() const | Specifies the operations that are allowed to a user on an encrypted PDF document. The default value is **DisallowAll**. |
| [get_UserPassword](./get_userpassword/)() const | Specifies the user password required for opening the encrypted PDF document. |
| [PdfEncryptionDetails](./pdfencryptiondetails/)(const System::String\&, const System::String\&) | Initializes an instance of this class. |
| [set_OwnerPassword](./set_ownerpassword/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfEncryptionDetails::get_OwnerPassword](./get_ownerpassword/). |
| [set_Permissions](./set_permissions/)(Aspose::Words::Saving::PdfPermissions) | Setter for [Aspose::Words::Saving::PdfEncryptionDetails::get_Permissions](./get_permissions/). |
| [set_UserPassword](./set_userpassword/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfEncryptionDetails::get_UserPassword](./get_userpassword/). |

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

